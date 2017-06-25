# ubuntu_x2go_firefox

## launch docker container
    docker run -d \
      --name x2go \
      -v /home/ec2-user/.ssh/authorized_keys:/home/foo/.ssh/authorized_keys \
      -p 2222:22 \
      nasoym/ubuntu_x2go_server

* forward ssh port 
  2222 to localhost 9999

* run x2go client
  /usr/bin/x2goclient 
    --session-conf=file
    --session=foobar
* session file:
    [20170214203951300]
    speed=0
    pack=8-jpeg
    quality=0
    name=foobar
    host=127.0.0.1
    user=foo
    key=/home/[user]/.ssh/[private key file]
    sshport=9999
    command=/usr/bin/firefox


