.. vale off

Command Line Interface (CLI) commands
#####################################

.. vale on

MailFly may require you to use the command line (CLI). Listed below are the available CLI commands.

.. note:: 

  You can find this list (and others - for example commands relating to Doctrine and other vendors) by running this command: ``bin/console``

  You must be in the MailFly root directory to run the CLI commands. 

**Format**: command [options] [arguments]

Options
=======

.. vale off

.. list-table:: 
   :widths: 50 50
   :header-rows: 1

   * - Options
     - Description
   * - -h, \--help
     - Display this help message
   * - -q, \--quiet
     - Do not output any message
   * - | V, \--version
       |  \--ansi
       |  \--no-ansi
     - | Display this app version
       | Force ANSI output
       | Disable ANSI output
   * - -n, \--no-interaction
     - 	Do not ask any interactive question
   * - | -s, \--shell
       |  \--process-isolation
     - | Launch the shell.
       | Launch commands from shell as a separate process.
   * - | -e, \--env=ENV
       |  \--no-debug
     - | The Environment name. [default: "prod"]
       |  Switches off debug mode.
   * - | -v
       | -vv
       | -vvv
       |  \--verbose
     - | Increase the verbosity of messages:
       | 1. for normal output,
       | 2. for more verbose output and
       | 3. for debug

       
.. vale on

MailFly commands
===============
These are the commands you may need to use in relation to your MailFly instance. Add a ``bin/console`` before MailFly command.

**Example**

.. code-block:: shell

  bin/console MailFly:segments:update

.. vale off

.. list-table:: 
   :widths: 25 50 25
   :header-rows: 1

   * - Command
     - Description
     - Aliases
   * - ``MailFly:assets:generate``
     - Combines and minifies Asset files (CSS/JS) from each bundle into single production files
     - 
   * - ``MailFly:broadcasts:send``
     - Process Contacts pending to receive a Channel broadcast.
     - 
   * - ``MailFly:campaigns:execute``
     - Execute specific scheduled events.
     - 
   * - ``MailFly:campaigns:rebuild``
     - Rebuild Campaigns based on Contact Segments.
     - ``MailFly:campaigns:update``
   * - ``MailFly:campaigns:trigger``
     - Trigger timed events for published Campaigns.
     - 
   * - ``MailFly:campaigns:validate``
     - Validate if a Contact has been inactive for a decision and execute events if so.
     - 
   * - ``MailFly:citrix:sync``
     - Synchronizes registrant information from Citrix products
     - 
   * - ``MailFly:cache:clear``
     - Clears MailFly cache, by using this command, you will erase the 10-minute MailFly cache, which contains things like segment counts and data for dashboard widgets.
     - 
   * - ``MailFly:contacts:deduplicate``
     - Merge Contacts based on same unique identifiers
     - 
   * - ``MailFly:custom-field:create-column``
     - Creates the actual column in the table
     - 
   * - ``MailFly:email:fetch``
     - Fetch and process monitored Email.
     - 
   * - ``messenger:consume email``
     - Processes mail queue
     - 
   * - ``MailFly:import``
     - If the CSV import is configured to run in background then this command will pick up the pending import jobs and imports the data from CSV files to MailFly.
     - 
   * - ``MailFly:integration:fetchleads``
     - Fetch Contacts from Integration.
     - ``MailFly:integration:synccontacts``
   * - ``MailFly:integration:pipedrive:fetch``
     - Pulls the data from Pipedrive and sends it to MailFly
     - 
   * - ``MailFly:integration:pipedrive:push``
     - 	Pushes the data from MailFly to Pipedrive
     - 
   * - ``MailFly:integration:pushleadactivity``
     - Push Contact activity to Integration. 
     - ``MailFly:integration:pushactivity``
   * - ``MailFly:install:data``
     - Installs data
     - 
   * - ``MailFly:iplookup:download``
     - Fetch remote datastores for IP lookup services that leverage local lookups.
     - 
   * - ``MailFly:maintenance:cleanup``
     - Cleans up older data.
     - 
   * - ``MailFly:messages:send``
     - Process sending of messages queue.
     - ``MailFly:campaigns:messagequeue``, ``MailFly:campaigns:messages``
   * - ``doctrine:migrations:generate``
     - Generate a blank migration class.
     - 
   * - ``MailFly:plugins:reload``
     - Install, reloads or updates Plugins.
     - ``MailFly:plugins:install``, ``MailFly:plugins:update``
   * - ``MailFly:queue:process``
     - Process queues
     - 
   * - ``MailFly:reports:scheduler``
     - Processes scheduler for Report's export
     - 
   * - ``MailFly:segments:update``
     - Update Contacts in smart Segments based on new Contact data.
     - ``MailFly:segments:rebuild``
   * - ``MailFly:theme:json-config``
     - Converts Theme config to JSON from PHP
     - 
   * - ``MailFly:unusedip:delete``
     - Deletes IP addresses that aren't used in any other database table
     - 
   * - ``MailFly:update:apply``
     - Updates the MailFly app.
     - 
   * - ``MailFly:update:find``
     - Fetches updates for MailFly
     - 
   * - ``MailFly:webhooks:process``
     - Process queued Webhook payloads
     - 
   * - ``social:monitor:twitter:hashtags``
     - Looks at the monitoring records and finds hashtags.
     - 
   * - ``social:monitor:twitter:mentions``
     - Searches for mentioned tweets
     - 

.. vale on

Doctrine commands
=================

.. list-table:: 
   :widths: 50 50
   :header-rows: 1

   * - Command
     - Description
   * - ``doctrine:fixtures:load``
     - Installs MailFly sample data, overwriting existing data.
