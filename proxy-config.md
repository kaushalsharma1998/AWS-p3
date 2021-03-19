- **_HAProxy configuration documentation requirements_**
    - What software / service needed to be installed ?
Ans.  In order to install the HAProxy I first ran the update command then installed the proxy by cloning the repository followed by the  apt-get install haproxy command.
    - What file(s) where modified & their location ?
    Ans  . The first file that has been modified to set up the load balancing is haproxy.cfg which is present as the location /etc/haproxy/haproxy.cfg
    - What configuration(s) were set
    The Default mode and log were delted because they worked on layer 7<br/>
    The frontend configuration was set to bind all the traffic on port 80<br>
    For the backend , mode was set to tcp and two server configuatons were provided.<br/> Webserver 1 has the IP: 35.171.221.88 <br/>
    Webserver 2 has the IP : 3.215.144.183<br/>



    - How to restart the service after a configuration change
    Ans. I restared the proxy using the command [systemctl restart haproxy]
    - Resources used (websites)
     https://www.haproxy.com/blog/the-four-essential-sections-of-an-haproxy-configuration/


  - **_Webserver 1 & 2 configuration documentation requirements_**
    - What software / service needed to be installed
    Ans. Both the web servers needed to have servers installed , I haved used Apache2 in both.
    - What file(s) where modified & their location
    Ans. The only file that was modified is index.html in both the servers and is present at [/var/www/html]
    - What configuration(s) were set (if any)
    No other configurations were set for this.
    - How to restart the service after a configuration change
    The service is restared by using the command  [systemctl restart apache2]
    - Resources used (websites)
    https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-ubuntu-20-04
  - **_Screenshot(s) indicative that by connecting to the proxy, the proxy is connecting to the webservers to serve content_**
  The image below shows how the HAProxy is working , for once it connects to server 1 and serves it's contents and again after 2-3 requests it jumps to server 2 and serves it's contents .
  Server 1 on haproxy
  <img width="964" alt="Subnet " src="/screenshotsp3/server1onhaproxy.png"><br />
  Server 2 on haproxy
  <img width="964" alt="VPC " src="/screenshotsp3/server2onhaproxy.png"><br/>


  - **_Link to your Elastic IP for your proxy_**
  http://54.82.111.140/
