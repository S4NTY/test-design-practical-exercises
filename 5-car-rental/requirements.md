# Requirements
## Car rental

**URL:** https://exercises.test-design.org/rental/

A rental company loans cars (EUR 300), and bikes (EUR 100) for a week.  
**R1** The customer can add cars or bikes one by one to the rental order.  
**R2** The customer can remove cars or bikes one by one from the rental order.  
**R3** If the customer rents cars for more than EUR 600, then they can rent one bike for free. In case of discount:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**R3a** If the customer has selected some bikes previously, then one of them becomes free.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**R3b** If the customer hasn't selected a bike previously, then one free bike is added.  
**R4** If the customer deletes some cars or motorcycles from the order that the offering threshold doesn't hold, then any offering will be withdrawn.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**R4a** When the discount is withdrawn but given again, and no bike was added meanwhile, the customer gets the previous discount back.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**R4b** When the discount is withdrawn and some bikes are added when the discount is given again, then one of them becomes free.  
**R5** If the customer deletes the free bike, then no money discount is given. Adding the bike back the discount is given again by converting the bike price to zero.   