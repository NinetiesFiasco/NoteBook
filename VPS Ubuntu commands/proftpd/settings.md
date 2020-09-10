  ### Настройки proftpd 
  #### `sudo nano /etc/proftpd/proftpd.conf`  
  
  `AllowOverwrite            on`  
  
  `RequireValidShell         off`  
  `AuthUserFile              /etc/proftpd/ftpd.passwd`  
  `AuthGroupFile             /etc/proftpd/ftpd.group`  
   
  `UseIPv6                   off`  
  `ServerName                "ftp-server"`  
  `ServerType                standalone`  
  `DeferWelcome              on`  


  ###Эти две команды убыстряют работу сервака, гуглите для подробностей.  
  `UseReverseDNS             off`  
  `IdentLookups              off`  

  `MultilineRFC2228          on`  
  `DefaultServer             on`  
  `ShowSymlinks              off`  

  `TimeoutNoTransfer         600`  
  `TimeoutStalled            100`  
  `TimeoutIdle               2200`  
 
  `DisplayChdir              .message`  
  `ListOptions               "-l"`  
 
  `TimeoutLogin              20`  
  
  `RootLogin                 off`  

  ### Журналы  
  `ExtendedLog               /var/log/ftp.log`  
  `TransferLog               /var/log/xferlog`  
  `SystemLog                 /var/log/syslog.log`  
  
  // **** ЭТУ ШТУКУ УДАЛИТЬ ****   
  // Запрещаем заливать файлы начинающиеся с точки  
  `DenyFilter                \*.*/`  
  //****************************   
  
  
  ### Сообщение после успешного захода на сервер  
  `AccessGrantMsg            "Welcome to Server"`  
  ### Идентификатор сервера, показывается всем при заходе на сервер  
  `ServerIdent                  on       "privet :))"`  
  
