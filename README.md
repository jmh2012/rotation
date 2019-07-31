# rotation

A command line utility for taking a server node in and out of service. 

## Configuration

Supports services with two load balancing types in rotation.conf: 

Servers load balanced with Level 4 healthchecks by enabling/disabling the service's TCP/UDP port using the system firewall. (Currently iptables is supported.)

Servers load balanced with Level 7 healthchecks by modifying a healthcheck file for healthchecks looking for an HTTP response code or content verification.

## Installation

Requires Python 2.6 - 3.x

Dependencies
```bash
pip install python-iptables

```
Setup
```bash
git clone <this repo>
cd rotation
vi rotation.conf # Configure the utility.
mv rotation.conf /etc/
mv rotation /usr/bin/
```

## Usage

```bash
rotation out # Take the server out of the load balancing pool.
rotation in # Put the server back in the load balancing pool.
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](https://choosealicense.com/licenses/mit/)
