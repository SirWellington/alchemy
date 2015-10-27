Alchemy [![Build Status](https://travis-ci.org/SirWellington/alchemy.svg)](https://travis-ci.org/SirWellington/alchemy)
==============================================

![Alchemy Logo](https://raw.githubusercontent.com/SirWellington/alchemy/develop/Graphics/Logo/Alchemy-Logo-v3-name.png)


### Making Java *fun* again.



# Alchemy Design

#### We take our inspiration from Mother Nature, specifically the four elements of nature. We call this, **Alchemy Design**.


# Earth

### Alchemy is as *Solid* and *Dependable* as Earth.

```java
assertThrows(() -> database.save(user));
```

We aim to provide you with libraries as **dependable** as the floor beneath your feet, that you implicitly trust to not collapse.
This means that our code is thoroughly tested early and often.

# Wind

### Alchemy is as *Swift* and *Undetectable* as Wind.

```java
String randomUsername = one(alphabeticStrings());
```

We strive to be **breezy** yet **inconspicuous** like Southern California winds.

We believe great code helps you get the job done, without getting in the way.


# Water

### Alchemy is as *Fluid* and *Simple* as Water.
```java
checkThat(firstName, lastName, username)
    .are(nonEmptyString())
    .are(stringWithLengthAtLeast(1));
```

The best code is **simple** and **fluid** as, a river flowing down a stream. It flows as you would intuitively expect.


# Fire

### Alchemy is as *Powerful* and *Invigorating* as Fire.

We want you to feel the power as it flows through your hands when you write code with us.

```java
Device newDevice = http.begin()
                       .body(device)
                       .post()
                       .expecting(String.class)
                       .at("https://iot.io/api/devices/");
```

These Design Principles guide the code that we write. As such you will see that many of our projects use the Fluid Language Style to make writing code more expressive and much closer to its English counterpart. We also want you to feel **good** when you write code with us. We want you to feel **powerful**.


# Project List

| Name | Purpose | Link
| -----| ----- | ------ |
| Alchemy Annotations   | Document
| Alchemy Arguments     | Check your assumptions
| Alchemy Generator     | Generate Data
| Alchemy Test          | Test your code
| Alchemy HTTP          | Call REST Services


## Highlights

### Test your code

>TODO: Add better examples

```java
//Generate random data
String name = one(alphabeticStrings());

//Quickly assert error conditions
assertThrows(() -> database.save(name))
    .isInstanceOf(IllegalArgumentException.class);
```

### Check your assumptions

```java
public int getTotalPointsForUser(String user) throws BadArgumentException, HttpException
{
    checkThat(user)
        .throwing(BadArgumentException.class)
        .is(notNull())
        .is(nonEmptyString())
        .is(stringWithLengthAtLeast(3));

    //Proceed safely...
}
```

### Call REST Services
```java


http.begin()
    .get()
    .usingQueryParam("device", id)
    .expecting(Device.class)
    .onSuccess(d -> LOG.info("Device created: {}", d))
    .onFailure(ex -> LOG.error("Failed to get device with ID {}", id))
    .at("https://iot.io/api/devices/query");
```

Just remember, this is only the beginning. These libraries will be continuously improved and updated.

## Requirements

+ Java 8
+ Maven

## Release Notes
> These release notes are for the pom.xml

### 1.1
+ Dependency Updates
+ Adding custom Javadoc Styling

### 1.0
+ Initial Release


## License

This Software, and all sub-projects, are licensed under the Apache 2.0 License

http://www.apache.org/licenses/LICENSE-2.0

<!-- Styling Code -->
<style>
h3 {
    color: #F85F73;
    font-size: 20px;
}
</style>
