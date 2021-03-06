
Services
========

Rockstor supports many services that are necessary for a storage system to be functional.
Service management including configuration, turning on or off, can be done via
the System tab of the web-ui.

In the web-ui, click on *System* tab to go to the *System* view. This also
serves as the *Services* view, which is selected by default in the left
sidebar. All services and their current state are displayed.

.. image:: services.png
   :scale: 70 %
   :align: center

To start or stop a service, click the ON or OFF buttons respecively.

Some services need to be configured before they can be turned on. To access the configuration page for a service, click the **wrench** icon next to the service name.

NFS
---

Rockstor uses Linux NFS server to support exporting Shares to remote clients
via NFS. Custom NFS configuration is not supported, but the service must be
turned on in order to export shares.

In the web-ui, click on *System* tab to go to the *System* view. This also
serves as the *Services* view, which is selected by default in the left
sidebar. To start or stop the NFS server, click the corresponding ON or OFF
button.

Samba
-----

Rockstor supports making Shares available to SMB and CIFS clients via Samba
software suite. Custom Samba server configuration is not supported, but the
service must be turned on before exposing shares.

In the web-ui, click on *System* tab to go to the *System* view. This also
serves as the *Services* view, which is selected by default in the left
sidebar. To start or stop the NFS server, click the corresponding ON or OFF
button.

NTP
---

NTP maintains system time in synchronization with Internet
standard time server. This service must always be turned on.

To configure NTP, you can specify the address of an Internet standard time
server in the NTP configuration page.

.. image:: ntp-config.png
   :scale: 70 %
   :align: center

AD
--

AD is a directory service to connect to Active Directory. It must be turned on
in order to be part of AD.

In the web-ui, click on *System* tab to go to the *System* view. This also
serves as the *Services* view, which is selected by default in the left
sidebar. To configure AD, click on the **wrench** icon and submit the form with
apropriate values as shown below.

.. image:: ad-config.png
   :scale: 70 %
   :align: center

The individual fields of the form are described below.

* **Domain**: Specifies the Windows Active Directory or domain controller to
  connect to.
* **Controllers**: domain controller to use.
* **Security**:  The security model to use, which configures how clients should
  respond to Samba. The options are

   1. user. A client must first log in with a valid username and password.
   2. server. In this mode, Samba will attempt to validate the username/password by authenticating it through another SMB server (for example, a Windows NT Server). If the attempt fails, the user mode will take effect instead.
   3. domain. In this mode, Samba will attempt to validate the username/password by authenticating it through a Windows NT Primary or Backup Domain Controller, similar to how a Windows NT Server would.
   4. ads. This mode instructs Samba to act as a domain member in an Active Directory Server (ADS) realm.

* **Realm**: When the ads Security Model is selected, this allows you to
  specify the ADS Realm the Samba server should act as a domain member of.
* **Template shell**: The login shell for the user
* **Allow offline login**

To start or stop the service, click the corresponding ON or OFF button.

LDAP
----

LDAP is a directory service to connect to LDAP server.

In the web-ui, click on *System* tab to go to the *System* view. This also
serves as the *Services* view, which is selected by default in the left
sidebar. To configure LDAP, click on the **wrench** icon and submit the form
with appropiate values as shown below.

.. image:: ldap-config.png
   :scale: 70 %
   :align: center

The individual fields of the form are described below.

* **LDAP Server**: The IP address of the LDAP server.
* **Search base DN**: Specifies that user information should be retrieved using
  the listed Distinguished Name (DN).
* **Enable TLS**: If this is checked, TLS will be used to encrypt passwords
  sent to the LDAP server.
* **Certificate URL**: If the ``Enable TLS`` checkbox is checked, you can
  specify a URL from which to download a valid CA (Certificate Authority)
  Ceritifcate. A valid CA Certificate must be in PEM (Privacy Enhanced Mail)
  format.

To start or stop the service, click the corresponding ON or OFF button.

NIS
---

NIS is a directory service to connect to a NIS server.

In the web-ui, click on *System* tab to go to the *System* view. This also
serves as the *Services* view, which is selected by default in the left
sidebar. To configure NIS, click on the **wrench** icon and submit the form
with appropiate values as shown below.

.. image:: nis-config.png
   :scale: 70 %
   :align: center

* **Domain**: NIS domain.
* **Server**: IP address of NIS server.

To start or stop the service, click the corresponding ON or OFF button.

