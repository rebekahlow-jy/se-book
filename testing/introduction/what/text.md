<link rel="stylesheet" href="{{baseUrl}}/css/textbook.css">

<div class="website-content">

<div id="path">Testing :arrow_right: Introduction :arrow_right:</div>

<div id="title">

#### What :one:

</div>

<div id="body">

> Testing is operating a system or component under specified conditions, observing or recording the results, and making an evaluation of some aspect of the system or component.  
>
> –- source: IEEE

<img src="{{baseUrl}}/testing/introduction/what/images/diagram.png" height="180" />
<p/>

Testing entails the execution of a set of test cases. A test case specifies how to perform a test. At a minimum, it specifies the input to the _software under test (SUT)_ and the expected behavior.

<tip-box>

Example: A minimal test case for testing a browser:

* **Input** – Start the browser using a blank page (vertical scrollbar disabled). Then, load ‘longfile.html’ located in the ‘test data’ folder.
* **Expected behavior** – The scrollbar should be automatically enabled upon loading ‘longfile.html’.

</tip-box>

Test cases can be determined based on the specification, reviewing similar existing systems, or comparing to the past behavior of the SUT.

<panel header="Other details a test case can contain :two:" type="seamless">

A more elaborate test case can have other details such as those given below.  

*	A unique identifier : e.g. TC0034-a
*	A descriptive name: e.g. vertical scrollbar activation for long web pages
*	Objectives: e.g. to check whether the vertical scrollbar is correctly activated when a long web page is loaded to the browser
*	Classification information: e.g. priority - medium, category - UI features
*	Cleanup, if any: e.g. empty the browser cache.

</panel>

For each test case we do the following:

1. Feed the input to the SUT
2. Observe the actual output
3. Compare actual output with the expected output

A test case _failure_ is a mismatch between the expected behavior and the actual behavior. A failure is caused by a _defect_ (or a bug).

<tip-box>

Example: In the browser example above, a test case failure is implied if the scrollbar remains disabled after loading ‘longfile.html’. The defect/bug causing that failure could be an uninitialized variable.

</tip-box>

<panel header="A deeper look at the definition of testing :three:" type="seamless">

Here is another definition of testing:

> Software testing consists of the _dynamic_ verification that a program provides _expected_ behaviors on a _finite_ set of test cases,
> suitably _selected_ from the usually infinite execution domain.
>
> -– source: SWEBOKv3

Some things to note (indicated by keywords in the above definition):

*	_Dynamic_: Testing involves executing the software. It is not by examining the code statically.
*	_Finite_: In most non-trivial cases there are potentially infinite test scenarios but resource constraints dictate that we can test only a finite number of scenarios.
*	_Selected_: In most cases it is not possible to test all scenarios. That means we need to select what scenarios to test.
*	_Expected_: Testing requires some knowledge of how the software is expected to behave.

</panel>

</div>

</div>
