*Step 1*

CFG graph for onClick() method in* https://github.com/BradTeachesCode/BasicCalculator/blob/master/BasicCalculator/app/src/main/java/com/bradteachescode/basiccalculator/MainActivity.java 

*Step 2*
**Node Coverage for CFG Graph:** 

*Test Requirements:*

-Start (Entry point) <br>
-onClick (Method entry)
-switch (Decision based on view.getId())
-key_0_btn to key_9_btn (Cases for number buttons)
-key_add_btn, key_sub_btn, key_div_btn, key_mult_btn (Cases for operation buttons)
-key_clear_btn (Case for clear button)
-key_equals_btn (Case for equals button)
-switch_symbol (Nested switch based on symbol)
-plus, minus, divide, multiply (Cases within nested switch)
-Reset (Resetting values)
-End (Exit point)

*Paths:* 
Start → onClick → switch → key_0_btn → End
Start → onClick → switch → key_1_btn → End
...
Start → onClick → switch → key_9_btn → End
Start → onClick → switch → key_add_btn → End
Start → onClick → switch → key_sub_btn → End
Start → onClick → switch → key_div_btn → End
Start → onClick → switch → key_mult_btn → End
Start → onClick → switch → key_clear_btn → End
Start → onClick → switch → key_equals_btn → switch_symbol → plus → Reset → End
Start → onClick → switch → key_equals_btn → switch_symbol → minus → Reset → End
Start → onClick → switch → key_equals_btn → switch_symbol → divide → Reset → End
Start → onClick → switch → key_equals_btn → switch_symbol → multiply → Reset → End
