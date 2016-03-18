These are a couple of Nagios plugins that I wrote simply to demonstrate knowledge of Python scripting and nagios monitoring, specifically in the context of a UNIX environment.

I built the plugins to monitor an app simulator (created specifically for practicing against), not a real production app. The app runs, but it doesn't do anything other than some basic "app stuff" to practice against such as forking PIDs, opening files, simulating transactions, etc.
The "instructions.txt" file shows the process I used to install the plugins and configure the nagios server to use them.


The plugin check_app_tx_response_time runs against a log file that has a specific format for the relevant lines containing the transaction times. That's why you see the large-ish regex expression in it.

The plugin check_app_open_files simply checks the open files of the primary app PID and all of it's child PIDs.