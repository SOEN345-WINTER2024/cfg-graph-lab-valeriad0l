# Lab 7
***By Valeria Dolgaliova (40212218)***

*Step 1*

CFG graph for onClick() method in https://github.com/BradTeachesCode/BasicCalculator/blob/master/BasicCalculator/app/src/main/java/com/bradteachescode/basiccalculator/MainActivity.java 

![Untitled Diagram-Page-3 drawio](https://github.com/SOEN345-WINTER2024/cfg-graph-lab-valeriad0l/assets/91857937/49fbfd0e-e587-40ae-9eb1-dccaa883a627)

*Step 2* <br>

**Node Coverage for CFG Graph** 

*Test Requirements:* <br>
-Start (Entry point) <br>
-onClick (Method entry) <br>
-switch (Decision based on view.getId()) <br>
-key_0_btn to key_9_btn (Cases for number buttons) <br>
-key_add_btn, key_sub_btn, key_div_btn, key_mult_btn (Cases for operation buttons) <br>
-key_clear_btn (Case for clear button) <br>
-key_equals_btn (Case for equals button) <br>
-switch_symbol (Nested switch based on symbol) <br>
-plus, minus, divide, multiply (Cases within nested switch) <br>
-Reset (Resetting values) <br>
-End (Exit point) <br>

*Paths:* <br>
Start → onClick → switch → key_0_btn → End <br>
Start → onClick → switch → key_1_btn → End <br>
... <br>
Start → onClick → switch → key_9_btn → End <br>
Start → onClick → switch → key_add_btn → End <br>
Start → onClick → switch → key_sub_btn → End <br>
Start → onClick → switch → key_div_btn → End <br>
Start → onClick → switch → key_mult_btn → End <br>
Start → onClick → switch → key_clear_btn → End <br>
Start → onClick → switch → key_equals_btn → switch_symbol → plus → Reset → End <br>
Start → onClick → switch → key_equals_btn → switch_symbol → minus → Reset → End <br>
Start → onClick → switch → key_equals_btn → switch_symbol → divide → Reset → End <br>
Start → onClick → switch → key_equals_btn → switch_symbol → multiply → Reset → End <br>

*Step 3* <br>

**Edge Coverage for CFG Graph**

*Test Requirements:* <br>
Start to onClick <br>
onClick to switch <br>
switch to each case (key_0_btn to key_9_btn, key_add_btn, key_sub_btn, key_div_btn, key_mult_btn, key_clear_btn, key_equals_btn) <br>
Each case back to the end or next decision point (for key_equals_btn, it goes to switch_symbol) <br>
switch_symbol to each case (plus, minus, divide, multiply) <br>
Each case within switch_symbol to Reset <br>
Reset to End <br>

*Paths:* <br>
Start → onClick → switch → key_0_btn → End <br>
Start → onClick → switch → key_1_btn → End <br>
... <br>
Start → onClick → switch → key_9_btn → End <br>
Start → onClick → switch → key_add_btn → End <br>
Start → onClick → switch → key_sub_btn → End <br>
Start → onClick → switch → key_div_btn → End <br>
Start → onClick → switch → key_mult_btn → End <br>
Start → onClick → switch → key_clear_btn → End <br>
Start → onClick → switch → key_equals_btn → switch_symbol → plus → Reset → End <br>
Start → onClick → switch → key_equals_btn → switch_symbol → minus → Reset → End <br>
Start → onClick → switch → key_equals_btn → switch_symbol → divide → Reset → End <br>
Start → onClick → switch → key_equals_btn → switch_symbol → multiply → Reset → End <br>

*Step 4* <br>

**Edge-Pair Coverage for CFG Graph**

*Test Requirements:* <br>
Start to onClick to switch  <br>
switch to each case and back to the end or next decision point  <br>
For key_equals_btn: switch to key_equals_btn, key_equals_btn to switch_symbol, and then switch_symbol to each case (plus, minus, divide, multiply)  <br>
Each case within switch_symbol to Reset, and Reset to End  <br>

*Paths:* <br>

Numeric Button to End: <br>
Start → onClick → switch → key_0_btn → End <br>
(Repeating for key_1_btn through key_9_btn) <br>

Operation Button to End: <br>
Start → onClick → switch → key_add_btn → End <br>
Start → onClick → switch → key_sub_btn → End <br>
Start → onClick → switch → key_div_btn → End <br>
Start → onClick → switch → key_mult_btn → End <br>

Clear Button to End: <br>
Start → onClick → switch → key_clear_btn → End <br>

Equals Button through Operations: <br>
Start → onClick → switch → key_equals_btn → switch_symbol → plus → Reset → End <br>
Start → onClick → switch → key_equals_btn → switch_symbol → minus → Reset → End <br>
Start → onClick → switch → key_equals_btn → switch_symbol → divide → Reset → End <br>
Start → onClick → switch → key_equals_btn → switch_symbol → multiply → Reset → End <br>

Sequential Operations (to cover edge pairs involving operations before key_equals_btn): <br>
Start → onClick → switch → key_add_btn → switch → key_equals_btn → switch_symbol → plus → Reset → End <br>
Start → onClick → switch → key_sub_btn → switch → key_equals_btn → switch_symbol → minus → Reset → End <br>
Start → onClick → switch → key_div_btn → switch → key_equals_btn → switch_symbol → divide → Reset → End <br>
Start → onClick → switch → key_mult_btn → switch → key_equals_btn → switch_symbol → multiply → Reset → End <br>
