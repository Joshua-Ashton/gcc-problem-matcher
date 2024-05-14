# gcc-problem-matcher with build dir support

## This is just gcc-problem-matcher but it ignores ../ at the start of the build dir

Github Action to [problem match](https://github.com/actions/toolkit/blob/master/docs/problem-matchers.md)
output from `gcc`. This allows warnings and errors from the compiler to be
prominently featured in pull requests like so:

![Matcher in action in pull request](/images/example-pull-request.png?raw=true)

This is a direct port of the `$gcc` rule from [vscode-cpptools](https://github.com/microsoft/vscode-cpptools).
Typical usage will be:

```yaml
    - uses: Joshua-Ashton/gcc-problem-matcher@master
    - name: Build Project
      run: make
```

**Note that this action does not build your code for you. It only makes the
errors and warnings from your compiler more prominent.**

## Development

Keep this up-to-date with the upstream vscode-cpptools `gcc` matcher:
https://github.com/microsoft/vscode-cpptools/blob/a8285cbc0efb5b09c2d2229b0e0772dcb3b602df/Extension/package.json#L76-L94

