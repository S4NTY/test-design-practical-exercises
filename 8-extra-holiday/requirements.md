# Requirements
## Extra holiday

**URL:** https://exercises.test-design.org/extra-holiday/

These requirements are the figment of imagination and not related to any real workplace 😊  
**R1** An employee can do overtime (overtime++).  
**R2** Doing overtime three times results in a free day (overtime = 0, free day++).  
**R3** An employee can take a free day by pressing – (free day--).  
**R4** If an employee is late, then one overtime is withdrawn (overtime--, if overtime = 0 → free day--, overtime = 2).  
**R5** If an employee takes three free days without lateness, then for the subsequent one-time lateness her accepted overtime remains unchanged.  
**R6** If an employee is late and overtime ≤ 0 and free days ≤ 0 then two overtimes are withdrawn (overtime = -2, free day = 0 → overtime = -1, free day = -1).  
**R7** If the number of free days is reduced to minus three, then GAME OVER!  

Test that the code satisfies the requirements.  