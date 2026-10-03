# Requirements
## University course grade system

**URL:** https://exercises.test-design.org/university-grade/

**R1** A university course grade system evaluates grades based on the following ingredients:  
- blackboard exercises (BE) in the range from 0 to 50 points,
- laboratory exercises (LE) in the range from 0 to 50 points,
- written part (WP), also in the range of 0 - 50 points,  

**R2** The sum of partial grades SUM = (BE + LE + WP) is calculated and the final grade follows the following rules:  
**R2-1** If any of BE, LE, WP is under 25 points - failed.  
**R2-2** SUM is less than 76 points – failed.  
**R2-3** SUM is 76 - 100 points - satisfactory.  
**R2-4** SUM is 101 - 125 points – good.  
**R2-5** SUM is greater than 125 points - very good.  

The output is the result set, i.e., failed/satisfactory/good/very good.   