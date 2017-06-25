# ubuntu_x2go_firefox

## launch docker container
    docker run -d \
      --name x2go \
      -v /home/ec2-user/.ssh/authorized_keys:/home/foo/.ssh/authorized_keys \
      -p 2222:22 \
      nasoym/ubuntu_x2go_server

