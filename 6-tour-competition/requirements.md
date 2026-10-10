# Requirements
## Tour competition

**URL:** https://exercises.test-design.org/tour-competition/

A tour competition application can handle registered teams as follows:  
**R1** During the registration process a unique team name together with globally unique team members can be entered. A team has at least one and at most three members. The registration is activated when ‘Add team’ is pressed.  
**R2** After entering an existing team name, missing team members can be added and existing team members can be deleted or modified.  
**R3** Members of incomplete teams can be ‘stolen’, i.e., they can be added to another team during registration or modification, only if the 'thief' team is complete.  
**R4** It is not allowed to construct a team only from 'stolen' members.  
**R5** If all the team members have been 'stolen' from a team, it’s deleted automatically, and no new team can be registered with the deleted team’s name.  
**R6** Stolen member cannot be modified only deleted. Stolen members can be further stolen from incomplete teams.  

For simplicity, authentication is ignored. Thus, if you enter an existing team name, it's a team modification. No test to validate team uniqueness is possible.