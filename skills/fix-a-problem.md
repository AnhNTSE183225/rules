Step 1: Create TODO list of below items
Step 2: Identify the problem. Capture error logs
Step 3: Perform static code check without execution: Where did the code failed?
Step 4: Add debugging logs, LOTS of debugging logs
Step 5: IF ONLY there is enough evidence from debugging logs, Fix ONE thing that fix the CORE issue - only ONE thing. IMPORTANT: Don't suppress errors, you must fix them from root cause.
Step 6: MUST Asks user to replicate the place of error again and wait for feedback. You are NOT allowed to replicate it yourself.
Step 7: If error again - IMPORTANT: REVERT the fix done in step 5 then repeat from step 1. If users' pasted logs isn't enough, add more debugging logs.
Step 8: If success, remove all debug logs added.