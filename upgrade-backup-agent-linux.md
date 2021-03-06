---

copyright:
  years: 1994, 2020
lastupdated: "2020-10-13"

keywords: IBM Cloud backup, EVault, Carbonite, backup, upgrade agent, Linux

subcollection: Backup

---
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:shortdesc: .shortdesc}
{:support: data-reuse='support'}
{:help: data-hd-content-type='help'}

# Upgrading backup software agent for Linux
{: #UpgradeinLinux}
{: help}
{: support}

Any agent that's older than the 8.50 version needs to be upgraded as they cannot connect with the Backup portal due to outdated, unsupported TLS functionality. Following the upgrade process ensures that you can upgrade your {{site.data.keyword.backup_notm}} agent without losing the registration.
{:shortdesc}

The most recent backup agent can be downloaded from your Cloud Backup Portal Dashboard quick links section.
{:tip}

1. Log in to your host at root level.
2. Download the latest version of the agent.
   ```
   wget -N downloads.service.softlayer.com/evault/Agent-Linux-x64-8.83.8124.tar.gz
   ```
   {:pre}

3. Extract the contents of the downloaded file.

   ```
   tar -xzvf Agent-Linux-x64-8.83.8124.tar.gz
   ```
4. Go to the recent installation directory.
   ```
   cd Agent-Linux-x64-8.83.8124/
   ```

5. Run installation script.
   ```
   ./install.sh
   ```
   {:pre}

6. Start answering the prompts by selecting your language. Then, if the current agent is registered in the Backup portal, select `N` for not registering the computer as a new host. If the current agent is not registered in the Backup portal, select `Y` complete the registration and provide the Portal address, {{site.data.keyword.backup_notm}} user ID and password. Lastly, select `A` to encrypt data by using the Integrated encryption method.

7. If the installation is successful, it is recorded in `/opt/BUAgent/Install.log`.
