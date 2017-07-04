<link rel="stylesheet" href="{{baseUrl}}/css/textbook.css">

<div class="website-content">

<div id="path">Error Handling :arrow_right: Defensive Programming :arrow_right:</div>

<div id="title">

#### Enforcing Compulsory Associations :two:

</div>

<div id="body">

Consider two classes, Account and Guarantor, with an association as shown in the following diagram:

<tip-box>

Example:

<img src="{{baseUrl}}/errorHandling/defensiveProgramming/compulsoryAssociations/images/accountGuarantor.png" height="50" />
<p/>

```java
class Account {
    Guarantor guarantor;

    void setGuarantor(Guarantor g) {
        guarantor = g;
    }
}
```

Here, the association is compulsory i.e. an `Account` object should always be linked to a `Guarantor`. One way to implement this is to simply use a reference variable as above. However, what if someone else in the team used the `Account` class as:

```java
Account a = new Account();
a.setGuarantor(null);
```

This results in an `Account` without a `Guarantor`! In a real banking system, this could have serious consequences! The code here did not try to prevent such a thing from happening. To proactively enforce the multiplicity constraint, a solution is offered as follows:

```java
class Account {
    private Guarantor guarantor;

    public Account(Guarantor g){
        if (g == null) stopSystemWithMessage(“multiplicity violated. Null Guarantor ”);
        guarantor = g;
    }
    public setGuarantor (Guarantor m){
        if (g == null) stopSystemWithMessage(“multiplicity violated. Null Guarantor”);
        guarantor = g;
    }
    …
}
```

In the class Account, `guarantor` has to be declared as a private variable to prevent the value from being changed from outside the class.

</tip-box>

<!-- extras ------------------------------------------------------------------------------------ -->

<panel header=":paperclip: Extras" expandable type="seamless" expanded>

  <panel header=":mortar_board: Learning Outcomes" expandable type="seamless">
    <include src="exercises.md" />
  </panel>

</panel>

</div>

</div>
