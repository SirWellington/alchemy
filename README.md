Alchemy [![Build Status](http://jenkins.redroma.tech/job/Alchemy/badge/icon)](http://jenkins.redroma.tech/job/Alchemy/)  [![Join the chat at https://gitter.im/SirWellington/alchemy](https://badges.gitter.im/SirWellington/alchemy.svg)](https://gitter.im/SirWellington/alchemy?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge) [![Aroma Enabled](http://brand.redroma.tech.s3-us-west-2.amazonaws.com/Badges/Aroma-Badge.svg)](http://aroma.redroma.tech/)
==============================================



![Alchemy Logo](https://raw.githubusercontent.com/SirWellington/alchemy/develop/Graphics/Logo/Alchemy-Logo-v7.png)


## Making Java *fun* again
Your kit for clean Java.

# Alchemy Design

#### We take our inspiration from Mother Nature, specifically the four elements of nature. We call this **Alchemy Design**.


# Earth
<img src="https://raw.githubusercontent.com/SirWellington/alchemy/develop/Graphics/Elements/Earth/Earth.png" width="400">

### Alchemy is *Solid* and *Dependable* like the Earth.

```java
assertThrows(() -> database.save(user))
    .isInstanceOf(SQLException.class);
```

We aim to provide you with libraries as **solid** and **dependable** as the floor beneath your feet that you implicitly trust to not collapse.
This means that our code is thoroughly tested early and often.

# Wind
<img src="https://raw.githubusercontent.com/SirWellington/alchemy/develop/Graphics/Elements/Wind/Wind.png" width="400">

### Alchemy is *Swift* and *Undetectable* like Wind.

```java
String randomUsername = one(alphabeticStrings());
```

We strive to be **breezy** yet **inconspicuous** like the air you breathe.

We believe great code helps you get the job done, without getting in the way.



# Water
 <img src="https://raw.githubusercontent.com/SirWellington/alchemy/develop/Graphics/Elements/Water/Water.png" width="400">


### Alchemy is *Fluid* and *Simple* like Water.
```java
checkThat(firstName, lastName, username)
    .are(nonEmptyString())
    .are(stringWithLengthAtLeast(1));
```

The best code is **simple** and **fluid** as a river flowing down a stream. It flows as you would intuitively expect.


# Fire
<img src="https://raw.githubusercontent.com/SirWellington/alchemy/develop/Graphics/Elements/Fire/Fire.png" width="400">

### Alchemy is *Powerful* and *Invigorating* like Fire.

We want you to feel the power as it flows through your hands when you write code with us.

```java
Coffee myCoffee = http.go()
					  .get()
					  .expecting(Coffee.class)
					  .at("http://aroma.coffee/orders?orderNumber=99");
```

These Design Principles guide the code that we write. As such you will see that many of our projects use the Fluid Language Style to make writing code more expressive and much closer to English. We also want you to feel **good** when you write code with us. We want you to feel **powerful**.


# Project List

| Name | Features
| -----| ----- |
| [Alchemy Annotations](https://github.com/SirWellington/alchemy-annotations) | Explicit Documentation              
| [Alchemy Arguments](https://github.com/SirWellington/alchemy-arguments)     | Check your assumptions    
| [Alchemy Collections](https://github.com/SirWellington/alchemy-collections) | Collect Yo'self    
| [Alchemy Generator](https://github.com/SirWellington/alchemy-generator)     | Generate Data
| [Alchemy Test](https://github.com/SirWellington/alchemy-test)               | Test your code
| [Alchemy HTTP](https://github.com/SirWellington/alchemy-http)               | Call REST Services
| [Alchemy HTTP Mock](https://github.com/SirWellington/alchemy-http-mock)     | Test your HTTP Code


## Highlights

### Generate Test Data

```java
String username = one(hexadecimalString());
int zipCode = one(integers(10_000, 99_999));
Computer computer = one(pojos(Computer.class));
```

### Test your code

```java
//Runs the test 50 times
@Repeat(50)
@Test
public void testDatabase()
{
    //Generate random data
    String name = one(alphabeticStrings());

    //Quickly assert error conditions
    assertThrows(() -> database.save(name))
        .isInstanceOf(SQLException.class);
}
```

### Check your assumptions

```java
public int getTotalPointsForUser(String user) throws HttpException
{
    checkThat(user)
        .is(notNull())
        .is(nonEmptyString())
        .is(stringWithLengthAtLeast(3))
        .is(userInDatabase()); //Custom Assertion

    //Proceed safely...
}
```

### Call REST Services

```java
Device newDevice = http.go()
                       .post()
                       .body(device)
                       .expecting(Device.class)
                       .at("https://iot.io/api/devices/");
```

Just remember, *this is only the beginning*. These libraries will be continuously improved and updated.

## Requirements

+ Java 8
+ Maven

## License

This Software, and all sub-projects, are licensed under the Apache 2.0 License

http://www.apache.org/licenses/LICENSE-2.0
