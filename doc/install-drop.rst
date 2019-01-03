.. _install-drop:

Install in the cloud
====================

Some people make you pay to have a 'cloud service'. What I'm providing here is a very simple way to install eLabFTW on your own server in the cloud, cutting the middleman.

This way you get to keep total control over your data. It will cost you less than 5$ a month. No setup fee, no annual licence, no overpriced features, welcome to open source software ;)

One other advantage is that you'll get your own server. With it, you can run whatever you want, not just eLabFTW! A `Wiki <https://www.mediawiki.org/wiki/MediaWiki>`_, a bug tracker, `GitLab <https://about.gitlab.com/>`_, etc…

Your eLabFTW installation will run in a `Docker <https://www.docker.com>`_ container. Learn more about eLabFTW in Docker :ref:`here <docker-doc>`.

Everything will be configured properly and automagically.

If you don't have a (sub)domain already, you can get one from `OVH <https://www.ovh.com>`_, `Gandi <https://www.gandi.net>`_, `1&1 <https://www.1and1.com>`_ or any other domain name registrar. You can get one for half a dollar per year. It is highly recommended to have a domain name, it's much more friendly than an IP addresses!

.. note:: If you don't want to deal with server administration or domain names and all these things, you can :doc:`use Nanobox.io to deploy eLabFTW <install-nanobox>`.

Create your droplet
-------------------

* Create an account on `DigitalOcean <https://m.do.co/c/c2ce8f861e0e>`_. Use this referral link to have 100$ offered!

* Alternatively, you can use `Vultr <http://www.vultr.com/?ref=7164540>`_. Use this referral link to register an account! The rest of this tutorial is for DigitalOcean.

.. image:: img/digitalocean.png
    :align: center
    :alt: digitalocean logo

* Create a droplet with Docker (from the One-click Apps tab), select a size and a region.

.. image:: img/docker-select.gif
    :align: center
    :alt: select docker app

* Optional: enable backups (might be a good idea)

* Optional but highly recommended: add your SSH key (`documentation <https://www.digitalocean.com/community/tutorials/how-to-use-ssh-keys-with-digitalocean-droplets>`_)

* Create the droplet (it takes less than a minute)

* Copy the IP address

* Optional: go to the control panel of your domain name provider. Point your domain (or subdomain) to the IP address of your drop. It might take a bit of time for the DNS to propagate (a few hours).

.. note:: Without a domain pointing to the drop, you will have a self signed certificate (so users will have a warning), whereas if you have a domain name, you will get a proper SSL certificate from Let's Encrypt.

Install eLabFTW
---------------

* Open a terminal and connect to your new server:

.. code-block:: bash

    ssh root@<DROPLET_IP_ADDRESS>

* Follow the :ref:`steps for a normal install <normal-install>`.


Video tutorial
--------------

This video shows all the steps from above:

.. raw:: html

    <iframe width="560" height="315" src="https://www.youtube.com/embed/K8CbQl7H5WA" frameborder="0" allowfullscreen></iframe>


