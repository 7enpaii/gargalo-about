# OK
* I resive the 200 status code if phone is confirmed

# Error
* I resive the 400 status code if is an error and the body
```json
{
  "errors": [
    "[!] The errors we give when the status code is 400 Bad request",
    "This password is not valid",
    "device_name field must be provided",
    "Password is not more than 7 chars"
  ]
}
```
