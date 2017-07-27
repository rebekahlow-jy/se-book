<panel header=":lock::key: Calculator">
<question>

A Calculator program crashes with an ‘assertion failure’ message when you try to find the square root of a negative number.

- [ ] a. This is a correct use of assertions.
- [ ] b. The application should have terminated with an exception instead.
- [ ] c. The program has a bug.
- [ ] d. All statements above are incorrect.

<div slot="answer">

- [ ] a. This is a correct use of assertions.
- [ ] b. The application should have terminated with an exception instead.
- [x] c. The program has a bug.
- [ ] d. All statements above are incorrect.

Explanation: An assertion failure indicates a bug in the code. (b) is not acceptable because of the word "terminated". The application should not fail at all for this input. But it could have used an exception to handle the situation internally.

</div>
</question>
</panel>
