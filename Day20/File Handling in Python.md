
# Day20- File Handling in Python

### Open a file in Python
- We use its built-in **open()** function. This function returns a file object, i.e., a handle. You can use it to read or modify the file.

```python
file object = open(file_name, [access_mode], [buffering])
```

### <file_name>
- It’s a string representing the name of the file we want to access.

### <access_mode>
- It’s an integer representing the file opening mode, e.g., read, write, append, etc. 

- It’s an optional parameter. By default, it is set to read-only <r>. In this mode, we get data in text form after reading from the file.

- The binary mode returns bytes. It’s preferable for accessing the non-text files like an image or the Exe files. See the table in the next section. It lists down the available access modes.

### \<buffering>

- The default value is 0, which means buffering won’t happen. 
- If the value is 1, then line buffering will take place while accessing the file. 
- If it’s higher than 1, then the buffering action will run as per the buffer size. In the case of a negative value, the default behavior is considered.


## File open modes in Python

| MODES |                                                                     DESCRIPTION                                                                    |
|:-----:|:----------------------------------:|
|  \<r>  | It opens a file in read-only mode while the file offset stays at the root.                                                                         |
|  \<rb> | It opens a file in (binary + read-only) modes. And the offset remains at the root level.                                                           |
|  <r+> | It opens the file in both (read + write) modes while the file offset is again at the root level.                                                   |
| <rb+> | It opens the file in (read + write + binary) modes. The file offset is again at the root level.                                                    |
|  \<w>  | It allows write-level access to a file. If the file already exists, then it’ll get overwritten. It’ll create a new file if the same doesn’t exist. |
|  \<wb> | Use it to open a file for writing in binary format. Same behavior as for write-only mode.                                                          |
|  <w+> | It opens a file in both (read + write) modes. Same behavior as for write-only mode.                                                                |
| <wb+> | It opens a file in (read + write + binary) modes. Same behavior as for write-only mode. |
|  \<a>  | It opens the file in append mode. The offset goes to the end of the file. If the file doesn’t exist, then it gets created.|
|  \<ab> | It opens a file in (append + binary) modes. Same behavior as for append mode. |
|  <a+> | It opens a file in (append + read) modes. Same behavior as for append mode.|
| <ab+> | It opens a file in (append + read + binary) modes. Same behavior as for append mode.|
|       |                                                                                                     |

## Close a file in Python
- It’s always the best practice to close a file when your work gets finished. However, Python runs a garbage collector to clean up the unused objects. But you must do it on your own instead leave it for the GC.
- We use python in-built close() function.
- While closing a file, the system frees up all resources allocated to it. And it’s rather easy to achieve.

```python
f = open("app.log",encoding = 'utf-8')
# do file operations.
f.close()
```