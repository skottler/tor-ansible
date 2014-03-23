# Setup a Tor relay with Ansible

This project will help you setup a Tor bridge relay (support for standard relays will come in the future) using [Ansible](http://ansible.com/). I am in no way responsible for any legal action or anything else that might happen to you as a result of running a Tor relay. You should read [this before proceeding](https://www.torproject.org/eff/tor-legal-faq.html.en). A simple sense of solidarity is great, but you should understand the technical and legal issues associated with participating in the Tor network before getting involved.

Getting started is really simple, but you'll need a few things:

1. A machine with ansible installed (available in most of the common package managers as 'ansible').
2. This git repo cloned onto your machine.
3. A virtual or physical machine running Ubuntu or Debian.

The machine you're going to turn into a Tor relay should have the root user configured with your SSH pubkey in `~/.ssh/authorized_keys`. Verify that you can login without using a password because the `common` role will configure sshd to only allow pubkey-based authentication.

Run ansible on the remote machine: `ansible-playbook -i "(remote IP or hostname)," -u root site.yml`. Make sure you've got the comma after the address of the machine.

## License
All the code in this repository is licensed under the GPLv3. Check out the LICENSE file in this repo for the complete text of the license.
