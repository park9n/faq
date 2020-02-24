## Category

### What should I read first?
- https://github.com/google/googletest/blob/master/googlemock/docs/for_dummies.md
- https://github.com/google/googletest/blob/master/googlemock/docs/cook_book.md

### Can I mock C-style function?
Yes, but not possible for variadic. Refer to https://github.com/google/googletest/blob/master/googlemock/docs/cook_book.md#mocking-free-functions and https://github.com/google/googletest/blob/master/googlemock/docs/gmock_faq.md#can-i-mock-a-variadic-function

### Can I do (2) stub method calls besides (1) verifying interactions? (`mockito` supports (1) and (2))
Possible to delegate calls to a fake. Refer to https://github.com/google/googletest/blob/master/googlemock/docs/cook_book.md#delegating-calls-to-a-fake-delegatingtofake
