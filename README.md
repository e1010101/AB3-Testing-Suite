# AB3-Testing-Suite
A small set of commands to test AB3


## Standard Procedure

* Download the latest JAR file from the team's releases page
* Put the JAR file in an empty folder in which the app is allowed to create files (i.e., do not use a write-protected folder)
* Open a command window. Run the java -version command to ensure you are using Java 11
* Check the UG to see if there are extra things you need to do before launching the JAR file, e.g., download another file from somewhere
* Launch the jar file using the java -jar command rather than double-clicking

## General AB-3 Related Tests

### AddCommand

#### Valid inputs

`add n/A very long name p/12345678 e/testmail@gmail.com a/AA Street t/testTag`

`add n/Amy Bee p/12345678 e/testmail@gmail.com a/AA Street`

#### Invalid inputs

Invalid Name

`add n/@@##!! p/12345678 e/testmail@gmail.com a/AA Street`

`add n/number 2 p/12345678 e/testmail@gmail.com a/AA Street`

Blank Name

`add n/ p/12345678 e/testmail@gmail.com a/AA Street`

No Name

`add p/12345678 e/testmail@gmail.com a/AA Street`

Invalid Phone

`add n/Amy Bee p/notAPhoneNumber e/testmail@gmail.com a/AA Street`

`add n/Amy Bee p/2 e/testmail@gmail.com a/AA Street`

Blank Phone

`add n/Amy Bee p/ e/testmail@gmail.com a/AA Street`

No Phone

`add n/Amy Bee e/testmail@gmail.com a/AA Street`

Blank Address

`add n/Amy Bee p/12345678 e/testmail@gmail.com a/`

Invalid Email

`add n/Amy Bee p/12345678 e/(testmail)@gmail.com a/AA Street`

`add n/Amy Bee p/12345678 e/####testmail@gmail.com a/AA Street`

`add n/Amy Bee p/12345678 e/testmail@gmail.com a/AA Street`

`add n/Amy Bee p/12345678 e/testmail@gmail.z a/AA Street`

`add n/Amy Bee p/12345678 e/testmail@gmail.#com# a/AA Street`

### EditCommand

#### Invalid inputs

`edit -1 n/Amy Bee`

`edit 0`

### Various DateTime Tests

#### Valid DatesTimes

`24-02-2022`

`24/02/2022`

`02/24/2022`

`24 Feb 2022`

`24 Feb 2022 13:00`

#### Invalid DateTimes

``

`    `

`!!! !!! !!!`

`Feb Feb Feb`

`31-02-2022`

`32/12/2022`

`12/32/2022`

`64 Feb 2022`

`24 Feb 2022 25:00`
