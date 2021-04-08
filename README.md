Click [here](https://github.com/Thalhammer/jwt-cpp) to the documentation of the original repo

I changed the implementation of `verify` in `jwt.h` to return a boolean value after a token has been verified. Useful if branching is needed after toke verification.

```
auto verifier = jwt::verify()
    .allow_algorithm(jwt::algorithm::hs256{ "secret" })
    .with_issuer("auth0");

// returns true or false
bool ok = verifier.verify(decoded_token); 
```
