---
tags: resume markdown babeljs es6
---


### projects

- `resume`
    - started a new "project" to overhaul my resume but it was in OpenOffice format which got me thinking ...
        1. what if I redid my resume in simple markdown and then render it as HTML, PDF, etc.
            - working pretty well
        2. what if I redid my resume as JSON
            - _issue_: single line strings for inherently multiline content **is a big bag full of hurt dropped on your toe**
                - _solution_: doesn't quite cut it... playing with the idea of using `babel` for ES6-style JSON (`.es6son`?)
            - _issue_: multiline strings work but keep the indention which is undesireable (want something like deindented here documents in `bash`)
                - _solution_: created a `deindent()` function to help
                - _result_: it takes a bit of machinery but it's nice to have
            - _issue_: now it has to be transpiled *AND* executed to produce the JSON ... almost there ...
                - _solution_: nevermind

```js
const FIRST_AND_LAST_LINE_RE = /^\s*\n|\n\s*$/g;

function getInnerLines(str) {
    return str.replace(FIRST_AND_LAST_LINE_RE, "");
}

//NOTE: could treat tabs/spaces differently if the user gives us a mapping (we'd use the computed indent size instead of raw indent string length)
const LEADING_WS_RE = /^(\s*).*$/gm;

function findIndent(str) {
    let indent, m;
    while ((m = LEADING_WS_RE.exec(str)) !== null && m.index !== str.length) {
        if (indent === undefined || m[1].length < indent.length) {
            indent = m[1];
        }
    }
    return indent;
}

function deindent(str) {
    let innerLines = getInnerLines(str),
        indent = findIndent(innerLines),
        indentRE = new RegExp("^" + indent, "gm");
    return innerLines.replace(indentRE, "");
}

const D = deindent;
export default {
    header: "uphill both ways",
    sections: [
        {
            header: "tech tid bits",
            sections: [
                D(`
                TEST:
                This is a test *of* _stuff_ ${1+2}.
                should be deindented.
                  ditto, but not all the way.
                  ditto that ditto, but not the trailing spaces on the last line ${""}
                `),
        }
    ],
};

console.log("%j", module.exports); //IT WORKS!

//NOTE: I'm not really using this but I can see how it it might come in handy in other places
//NOTE: could maybe create ES6 templated string tag function for this
```
