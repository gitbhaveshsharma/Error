### 🚫 Error: Address already in use (EADDRINUSE)

**Description:**
The error occurred while attempting to start the server, as the specified port `3001` is already in use by another process. This commonly happens when multiple applications try to bind to the same port.

**Error Message:**
```
  code: 'EADDRINUSE',
  errno: -4091,
  syscall: 'listen',
  address: '::',
  port: 3001
}
```

**Solution:**
1. **Find and Kill the Process:**
   - Use the `lsof -i :3001` command to identify the process(es) using port `3001`.
   - Terminate the process using `kill <PID>`.

2. **Change the Port:**
   - Modify your application code to listen on a different port.
   - Update the port number in your code to an available port (e.g., `3002`).

### GitHub Readme Note:
If you encounter the "Error: listen EADDRINUSE", it means the port your application is trying to use is already in use. To resolve this, you can either terminate the process using the port or modify your application to use a different port. Follow the instructions provided to resolve the issue.
