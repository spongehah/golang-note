## fmt

- 输入一行的内容并赋值给变量：

  ```go
  var msg string
  fmt.Scanln(&msg)
  ```

## strings

- 以某个字符串分割成数组：

  ```go
  strings.Split()
  ```

- 去掉字符串两端的某些字符：

  ```go
  strings.Trim()
  //去掉两端的空格：
  strings.TrimSpace()
  ```

- 将字符串拆分为单词数组：

  ```go
  strings.Fields()
  ```

## io

- socket通信时，监听对端的消息并打印到控制台的简写：

  ```go
  //一旦client.conn有数据，就直接copy到stdout的标准输出上，永久阻塞监听
  io.Copy(os.Stdout, this.conn)
  
  //等价于下面几句：
  //for {
  //  buf := make([]byte, 4096)
  //  n, err := this.conn.Read(buf)
  //  fmt.Println(string(buf[:n-1]))
  //}
  ```

  