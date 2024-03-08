*Step 1*

CFG graph for onClick() method in* https://github.com/BradTeachesCode/BasicCalculator/blob/master/BasicCalculator/app/src/main/java/com/bradteachescode/basiccalculator/MainActivity.java 

*Step 2* <br>

**Node Coverage for CFG Graph:** 

*Test Requirements:*

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

*Paths:* 
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
