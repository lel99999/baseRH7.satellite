# baseRH7.satellite
RedHat 7 Satellite Build and Config

### Ports for Browser-based User Interface Access to Satellite
|Port   | .   Protocol .   |  Service .  | .           Required For .           |
| ----- | ---------------- | ----------- | ------------------------------------ |
|443 .  | .   TCP .        | HTTPS       | Browser-based UI access to Satellite |
|80 | TCP . | HTTP | Redirection to HTTPS for web UI access to Satellite (optional) |


### Ports for Client to Satellite Communication
|Port   | .   Protocol .   |  Service .  | .           Required For .           |
| ----- | ---------------- | ----------- | ------------------------------------ |
| 80 | TCP | HTTP | Anaconda, yum, for obtaining Katello certificates, templates, and for downloading IPXE firmware |
| 443 | TCP | HTTPS | Subscription Management Services, yum, Telemetry Services, and for connection to the Katello Agent |
| 5647 | TCP | amqp | The Katello Agent to communicate with the Satellite’s Qpid dispatch router |
| 8000 | TCP | HTTPS | Anaconda to download kickstart templates to hosts, and for downloading iPXE firmware |
| 8140 | TCP | HTTPS | Puppet agent to Puppet master connections |
| 9090 | TCP | HTTPS | Sending SCAP reports to the Smart Proxy in the integrated Capsule and for the discovery image during provisioning |
| 5000 | TCP | HTTPS | Connection to Katello for the Docker registry |
