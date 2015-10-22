The Alchemy Collection [![Build Status](https://travis-ci.org/SirWellington/alchemy.svg)](https://travis-ci.org/SirWellington/alchemy)
==============================================

### Making Java *fun* again.




# Alchemy Design

#### We take our inspiration from Mother Nature, specifically the four elements of nature. We call this, **Alchemy Design**.

# Earth

### Alchemy is as *Solid* and *Dependable* as Earth.

We aim to provide you with libraries as dependable as the floor beneath your feet that you implicitly trust to not collapse.
This means that our code is thoroughly tested early and often.


# Wind

### Alchemy is as *Swift* and *Undetectable* as Wind.

# Water

### Alchemy is as *Fluid* and *Simple* as Water.

# Fire

### Alchemy is as *Powerful* and *Invigorating* as Fire.


# Project List

## Highlights

### Test your code

>TODO: Add better examples

```java
String name = one(alphabeticStrings());

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
String id = http.begin()
                .body(device)
                .post()
                .expecting(String.class)
                .at("https://iot.io/api/devices/");

http.begin()
    .get()
    .usingQueryParam("device", id)
    .expecting(Device.class)
    .onSuccess(d -> LOG.info("Device created: {}", d))
    .onFailure(ex -> LOG.error("Failed to get device with ID {}", id))
    .at("https://iot.io/api/devices/query");
```

## Requirements

+ Java 8
+ Maven

## Release Notes

### 1.0
+ Initial Release


## License

This Software, and all sub-projects, are licensed under the Apache 2.0 License

http://www.apache.org/licenses/LICENSE-2.0
