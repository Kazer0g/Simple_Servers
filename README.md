# Simple_Servers

## Python
[main.py](Python/main.py)
```python
import socket

server = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
server.bind (('127.0.0.1', 2000))

server.listen(4)

print ('Working...')

client_socket, address = server.accept()

data = client_socket.recv(1024).decode('utf-8')
print (data)

client_socket.send('Connected'.encode('utf-8'))
```

## C\#
## Rust
## Pascal
## C
## C++
## Java
[server.java](Java/server.java)
```java
import java.net.*;
import java.io.*;

public class server{
    public static void main(String[] args) throws IOException {
        ServerSocket ss = new ServerSocket(2000);
        Socket s = ss.accept();

        System.out.println("Connected");

        InputStreamReader in = new InputStreamReader(s.getInputStream());
        BufferedReader bf = new BufferedReader(in);

        String str = bf.readLine();
        System.out.println("client" + str);

        PrintWriter pr = new PrintWriter(s.getOutputStream());
        pr.println(str+str);
        pr.flush();
        
    }
}
```
## ASM
## NodeJs
## Ruby
## Erlang
## Go

## Haskell