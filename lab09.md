# 自顶向下，逐步求精

自顶向下，逐步求精就是要将一个问题的解决分为若干个小步骤，在一点一点的完成每一个步骤，从而实现问题的完全解决。
接下来我们就用洗衣机的案例做示范：
***
首先，我们写出要进行的步骤

一、注水

二、洗涤

三、漂洗

四、脱水


begin

input 水量 

water_in_switch（open）

if（现水量>=输入水量）

water_in_switch(close)

end if

while(time_counter为4的倍数）

    if（电机正在左转）

    motor_run（right）

    else（电机正在右转）

    motor_run（left）

    end if

    if（time_counter()>=一定时间）

    结束循环

motor_run(stop)

water_out_switch(open)

if(水量不变即水无法排出）

water_out_switch(close)

发出警报声

halt

else

继续程序

end if

repeat

    if（水流极小）

    water_out_switch(close)

    water_in_switch（open）

    if（现水量>=输入水量）

    water_in_switch(close)
    end if

    water_out_switch(open)

    if(水量不变即水无法排出）

    water_out_switch(close)

    发出警报声

    halt

    else

    继续程序

    end if

until（水的ph值达到干净标准）

do

motor_run（left）

until（水流极小）

then 

发出警报

halt

## 在整个过程中，我们可以从没各大环节中找到小的部分进行完善和修改，这就是自顶向下，逐步求精的方法