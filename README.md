**Windows Users:**

1. Install xming:

[Xming X Server for Windows download | SourceForge.net](https://sourceforge.net/projects/xming/)

1. Start xming. It will run in the background.

![](RackMultipart20221012-1-vfr2f2_html_5aa4ae62e8d7fac9.png)

1. SSH into the machine:

set DISPLAY=localhost:0.0

ssh -AYC {kerberos}@{machine}.cse.iitd.ac.in

**Use your GCL password and not Kerberos password**

Refer to the end of the doc for how to choose a machine to ssh to.

Ex:

ssh -AYC cs5190421@jhelum.cse.iitd.ac.in

ssh -AYC cs5190421@yamuna.cse.iitd.ac.in

![](RackMultipart20221012-1-vfr2f2_html_48bd730049fd98a1.png)

![](RackMultipart20221012-1-vfr2f2_html_84f874154a81132d.png)

**Linux Users:**

ssh -X {kerberos}@{machine}.cse.iitd.ac.in

**Use your GCL password and not Kerberos password**

Refer to the end of the doc for how to choose a machine to ssh to.

Ex:

ssh -X cs5190421@jhelum.cse.iitd.ac.in

ssh -X cs5190421@yamuna.cse.iitd.ac.in

**How to choose a machine to ssh?**

There are seven servers available:

1. godavari
2. jhelum
3. narmada
4. yamuna
5. ganga
6. satluj
7. hooghly

Choose the server with an index = (last five digits of entry number modulo seven) + 1.

Ex:

Entry number = 2019CS50421

Last five digits = 50421

Modulo value = 50421%7 = 0

Hence, I will choose 0+1= the 1st server.

ssh -AYC cs5190421@godavari.cse.iitd.ac.in
