![](/assets/volume-add2.png)

# **dcoker file: volume**![](/assets/volume-dockerfile1.png)

# **Example docker file:**

`# volume test`

`FROM centos`

`VOLUME ["/dataVolumeContainer1","/dataVolumeContainer2"]`

`CMD echo "finished,--------success1"`

`CMD /bin/bash`



# Example docker build:![](/assets/volume-dockerbuild.png)

# Example docker run:![](/assets/volume-dcokerrun.png)

# Tips：

![](/assets/volume-tips.png)



