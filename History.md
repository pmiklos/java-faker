Java Faker

0.6
---
- Added detailed credit card numbers that pass the luhn check.

```
faker.finance().creditCard();
```

0.5
---
- IDN support
- Stripped out quotes for domain names
- Added timezone support for addresses

0.4
---
* Some API changes

    * fetch/fetchString/fetchObject methods are no longer accessible from the Faker class

    * New way to access data generation methods is not directly from the Faker class

So

```
faker.name().firstName(); // preferred
```

instead of

```
faker.firstName(); // deleted
```


* Added email address in
```
faker.internet().emailAddress();
```
* Finnish locale support
* Ability to pass in Random object to control seeding

```
new Faker(random);
```

* Credit card faker data added

```
new Faker().business().creditCardNumber();
```

* Migrated over to using SnakeYAML instead of JYaml as the latter is no longer being maintained
* Bit of an internal refactor
* Added fixedString
```
faker.lorem().fixedString(int);
```

* Added the ability to generate URLs.
```
faker.internet().url();
```

* Added the ability to get one option of a input set
```
faker.options().option(String[]);
```

=======
* Added latitude and longitude

```
new Faker().address().latitude();
```

```
new Faker().address().longitude();
```
