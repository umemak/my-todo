# my-todo


```sh
error[E0308]: mismatched types
  --> src\handlers.rs:41:5
   |
39 | ) -> Result<impl IntoResponse, StatusCode> {
   |      ------------------------------------- expected `Result<_, StatusCode>` because of return type
40 |     todo!();
41 |     Ok(StatusCode::OK)
   |     ^^^^^^^^^^^^^^^^^^ expected `Result<_, StatusCode>`, found `Result<StatusCode, Error>`
   |
   = note: expected enum `Result<_, StatusCode>`
              found enum `Result<StatusCode, anyhow::Error>`
help: try wrapping the expression in `Ok`
   |
41 |     Ok(Ok(StatusCode::OK))
   |     +++                  +
```
