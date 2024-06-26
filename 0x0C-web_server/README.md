# 0x0C. Web server

| Concepts                                                                                   |
| ------------------------------------------------------------------------------------------ |
| For this project, we expect you to look at this concept:                                   |
| * [What is a Child Process?](https://github.com/Amyn00/alx-concepts/blob/main/CHILD_PROCESS.md).                                                                                         |

<img src="https://github.com/Amyn00/alx-system_engineering-devops/blob/master/0x0C-web_server/images/server.png">

## Background Context

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/AZg4uJkEa-4/0.jpg)](https://www.youtube.com/watch?v=AZg4uJkEa-4)

In this project, some of the tasks will be graded on 2 aspects:

1. Is your `web-01` server configured according to requirements
2. Does your answer file contain a Bash script that automatically performs commands to configure an Ubuntu machine to fit requirements (meaning without any human intervention)

For example, if I need to create a file `/tmp/test` containing the string `hello world` and modify the configuration of Nginx to listen on port `8080` instead of `80`, I can use `emacs` on my server to create the file and to modify the Nginx configuration file `/etc/nginx/sites-enabled/default`.

But my answer file would contain:
```bash
sylvain@ubuntu cat 88-script_example
#!/usr/bin/env bash
# Configuring a server with specification XYZ
echo hello world > /tmp/test
sed -i 's/80/8080/g' /etc/nginx/sites-enabled/default
sylvain@ubuntu
```
As you can tell, I am not using `emacs` to perform the task in my answer file. This exercise is aiming at training you on automating your work. If you can automate tasks that you do manually, you can then automate yourself out of repetitive tasks and focus your energy on something more interesting. For an [SRE](https://www.atlassian.com/incident-management/devops/sre), that comes very handy when there are hundreds or thousands of servers to manage, the work cannot be only done manually. Note that the checker will execute your script as the `root` user, you do not need to use the `sudo` command.

A good Software Engineer is a [lazy Software Engineer](https://www.techwell.com/techwell-insights/2013/12/why-best-programmers-are-lazy-and-act-dumb).

<img src="https://github.com/Amyn00/alx-system_engineering-devops/blob/master/0x0C-web_server/images/imge.jpg">

Tips: to test your answer Bash script, feel free to reproduce the checker environment:

* start a `Ubuntu 16.04` sandbox
* run your script on it
* see how it behaves

## Resources

**Read or watch:**

* [How the web works](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works)
* [Nginx](https://en.wikipedia.org/wiki/Nginx)
* [How to Configure Nginx](https://www.digitalocean.com/community/tutorials/how-to-set-up-nginx-server-blocks-virtual-hosts-on-ubuntu-16-04)
* [Child process concept page](https://github.com/Amyn00/alx-system_engineering-devops/blob/master/0x0C-web_server/CHILD_PROCESS.md)
* [Root and sub domain](https://landingi.com/help/domains-vs-subdomains/)
* [HTTP requests](https://www.tutorialspoint.com/http/http_methods.htm)
* [HTTP redirection](https://moz.com/learn/seo/redirection)
* [Not found HTTP response code](https://en.wikipedia.org/wiki/HTTP_404)
* [Logs files on Linux](https://www.cyberciti.biz/faq/ubuntu-linux-gnome-system-log-viewer/)

**For reference:**

* [RFC 7231 (HTTP/1.1)](https://datatracker.ietf.org/doc/html/rfc7231)
* [RFC 7540 (HTTP/2)](https://datatracker.ietf.org/doc/html/rfc7540)

**man or help:**

* `scp`
* `curl`

## Learning Objectives

### General

* What is the main role of a web server
* What is a child process
* Why web servers usually have a parent process and child processes
* What are the main HTTP requests

### DNS

* What DNS stands for
* What is DNS main role

### DNS Record Types

* `A`
* `CNAME`
* `TXT`
* `MX`

### Copyright - Plagiarism

* You are tasked to come up with solutions for the tasks below yourself to meet with the above learning objectives.
* You will not be able to meet the objectives of this or any following project by copying and pasting someone else’s work.
* You are not allowed to publish any content of this project.
* Any form of plagiarism is strictly forbidden and will result in removal from the program.

## Requirements
### General

* Allowed editors: `vi`, `vim`, `emacs`
* All your files will be interpreted on Ubuntu 16.04 LTS
* All your files should end with a new line
* A `README.md` file, at the root of the folder of the project, is mandatory
* All your Bash script files must be executable
* Your Bash script must pass `Shellcheck` (version `0.3.7`) without any error
* The first line of all your Bash scripts should be exactly `#!/usr/bin/env bash`
* The second line of all your Bash scripts should be a comment explaining what is the script doing
* You can’t use `systemctl` for restarting a process

