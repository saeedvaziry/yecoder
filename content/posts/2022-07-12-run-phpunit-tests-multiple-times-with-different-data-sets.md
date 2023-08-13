---
title: 'Run PHPUnit tests, multiple times with different data sets'
date: '2022-07-12T13:28:00+00:00'
author: Saeed Vaziry
layout: post
url: /posts/run-phpunit-tests-multiple-times-with-different-data-sets/
categories:
    - PHP
    - PHPUnit
    - Tests
tags:
    - php
    - phpunit
    - tests
---

So most of you might know this, Specially you old-school PHP developers 🙂 but it’s not gonna fill the internet’s capacity so let me be happy by writing this post.

You might have seen some PHPUnit tests with arguments! Have you asked yourself how it’s possible and who sends those arguments to these tests? The answer is simple! **Data Providers**

With PHPUnit, you can define arguments for your test function, and in the DocBlock you mention that there is a data provider for this function, and inside that function just provide the data 🙂

So we have a test function like this:

```php
/**
* @dataProvider provider
*/
function test_something_dummy($foo, $bar)
{
    $this->assertEquals($foo, $bar);
}
```

And now you just need to create that `provider` function to provide the `$foo` and `$bar` arguments.

```php
function provider()
{
    return [
        ['a', 'b'],
        ['X', 'X'],
        // repeat as many as you want</em>
    ];
}
```

So in this case your test will be executed twice with the following data

```php
test_something_dummy('a', 'b'); // fails

test_something_dummy('X', 'X'); // passes
```

So simple hah? Don’t forget to check the [official documentation](https://phpunit.de/manual/3.7/en/writing-tests-for-phpunit.html#writing-tests-for-phpunit.data-providers).

Make me happy with your comments 🙂 or even happier by subscribing to my blog’s newsletter 😁

See you in the next post 👋