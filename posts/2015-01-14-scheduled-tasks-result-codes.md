
List of windows scheduled task result codes below

  * 0 or 0x0: The operation completed successfully.
  * 1 or 0x1: Incorrect function called or unknown function called.
  * 2 or 0x2: File not found.
  * 10 or 0xa: The environment is incorrect.
  * 0x41300: Task is ready to run at its next scheduled time.
  * 0x41301: Task is currently running.
  * 0x41302: Task is disabled.
  * 0x41303: Task has not yet run.
  * 0x41304: There are no more runs scheduled for this task.
  * 0x41306: Task is terminated.
  * 0x8004130F: Credentials became corrupted [(*)](http://support.microsoft.com/kb/328773 "Task schedular corrupted credentials.")
  * 0x8004131F: An instance of this task is already running.
  * 0x80070002: Basically something like file not available (2147942402)
  * 0x800704DD: The service is not available (is &#8216;Run only when an user is logged on&#8217; checked?)
  * 0xC000013A: The application terminated as a result of a CTRL+C.
  * 0xC06D007E: Unknown software exception

and useful links to troubleshoot scheduled task issues

  * <a href="http://msdn.microsoft.com/en-us/library/aa383604" target="_blank" rel="noopener noreferrer">Task Scheduler Error and Success Constants</a>
  * <a href="http://support.microsoft.com/kb/308558" target="_blank" rel="noopener noreferrer">How to troubleshoot scheduled tasks in Windows XP and in Windows Server 2003</a>