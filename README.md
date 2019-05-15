# Python Server

* A server that stores key-value pairs.
* Jupyter Notebook
* Python 3

## Request Format

- `GET key` - this requests the value associated with key
   - The response code is 404 if the key doesn’t exist
- `PUT [key] [value]` - this requests that the server associates value with key
- `DELETE [key]` - this removes the key-value pair from the table
   - Even if key is not stored, the response code can be 200 OK
- `CLEAR` - this clears the table of all key-value pairs
- `QUIT` - will gracefully terminate the connection and let the server accept another one

## Response Format

- `200 OK` - request is valid and has been completed
- `220 UNSUPPORTED` - operation not recognized
- `400 BAD_REQUEST` - operation recognized, but not properly formatted
(missing/invalid args, etc.)
- `404 NOT FOUND` - specified key was not found for GET

```python
PuTTy:
localhost
8000
```
