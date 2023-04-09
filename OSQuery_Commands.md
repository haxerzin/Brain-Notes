# OSQuery Commands

## See all tables heading

> .tables

## See all columns fom schema

> . schema tablename
 
## See system info

> select * from system_info;

## See users

> select username,uid,shell from users;		

## See a process with multi table join and suspesious and their services

> select p.name,p.path,pp.name as parentname, pp.path as parentpath from processes as p left outer join processes as pp on p.parent=pp.pid order by p.name;

## Check process other than services are vulnerable

> select name,pid,path,display_name from services where start_type = 'auto_start' and path not like 'C:\Windows\System32\svchost.exe -k %';

## See install location for program

> select name,install_location from programs;

## See specific installed apps

> select name,install_location from programs where name like '%brave%';

## See user directory

> select uid,username,shell,directory from users;

## See auto startup

> select name,path,source,status from startup_items where path not like '%desktop.ini%';

## See registery data

> select dATA from registry where key like '(type or copy paste registry location)';

## See admin level users

> select users.uid,users.username,shell from user_groups inner join users on user_groups.uid = users.uid where user_groups.gid = 544;

## See browser extention

> select * from chrome_extensions;

## See browser extension permisions

> select name,permissions from chrome_extensions;

## Check threats via shim based id

> select executable,path,description,sdb_id from appcompat_shims;

## Check network based web server problems

> select name, cwd, parent, pid from processes;

## Check network based problems on a specific app

> select name, cwd, parent, pid from processes where name like '%brave.exe%';

## Check processes open from remote machine by cmdline

> select name, cwd, parent, cmdline pid from processes where name like '%brave.exe%' limit 1;

## See active listening ports

> select distinct processes.pid, listening_ports.port,processes.name from processes left join listening_ports using (pid);
