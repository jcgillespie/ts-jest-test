# ts-jest-test
Test case for debugging Jest tests written in Typescript 

Steps to reproduce
1. `yarn` or `npm install` to install dependencies
2. Set breakpoint on line 6 of `SystemUnderTest.spec.ts`. (Just above `debugger;` statement)
3. Set breakpoint on line 3 of `SystemUnderTest.ts`. (Inside `constructor`).
4. Press F5 or click "Start Debugging".

# Expected Behavior
Debugger should stop...
1. On line 6 of `SystemUnderTest.spec.ts`.
2. On line 3 of `SystemUnderTest.ts`.
3. On line 7 of `SystemUnderTest.spec.ts`.

# Actual Behavior
Debugger only stops on line 7 of `SystemUnderTest.spec.ts`

# Additional observations
VS Code reports that the breakpoints are loaded. They are not greyed out.

![breakpoints](http://i.imgur.com/EHYMjG1.png)

However, as the debugger reaches each expected breakpoint but doesn't it it, it will begin reporting a source map problem.

![sourcemaps](http://i.imgur.com/g0m3P7J.png)

The "future" breakpoint (line 8 of `SystemUnderTest.spec.ts`) does not report any sourcemap problem.