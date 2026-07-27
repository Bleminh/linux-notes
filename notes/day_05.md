1. ps (Processes)
- "ps" command provides a quick snapshot of the processes associated with your current terminal session.
- PID = process ID. Typically assigned sequentially.
- TTY: controlling terminal for the process.
- TIME: The total CPU time the process has used.
- CMD: The command that started the process.
- ps aux
- ps -ef
- "top" command provides a real-time, dynamic view of the processes on your system.
2. kill (Terminate)
- kill PID -> standard way to ask a program to terminate
- Ex: kill -15 12445 equivalent to kill 12445
- Forcing Termination: kill -9 12445
- signal 1: reload configuration files
- signal 2: interupt the process current operation
- signal 19: pause the process
- signal 0: check process existance
3. Job Control:
- To start a process directly in the background, simply append an ampersand (&) to your command.
sleep 1000 &
sleep 1001 &
sleep 1002 &
- "jobs" command: View all the jobs running in the background.