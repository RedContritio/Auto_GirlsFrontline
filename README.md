# Auto_GirlsFrontline
少女前线的中国特色社会主义现代化：全自动拖尸、后勤、打捞、捡垃圾

# 责任声明
本程序为个人为了减轻负担而创造的兴趣产物，在此分享给大家学习使用，造成的一切后果与我无关，如若侵权请联系我删除

# 功能介绍
当前上传了四个功能：
1. auto0_2: 自动0-2拖尸
2. autoLSupport：自动收后勤
3. auto4_6: 自动4-6捡垃圾（初级、中级资料）
4. autoJS9: 冬活干涉仪II捞JS9/白金勋章

8-1n我现在还没有两只zas，等有了再做；过几个月练度高了看看能不能去12-4e，能去就也做一个

# 使用说明
1. 此项目中的所有程序仅能在电脑端配合模拟器使用 
2. 运行时请务必"以管理员运行"，不然权限不够会报错的
3. 本程序是.py脚本，不是.exe那中直接双击运行的，需要你懂python编程基础的才能使用，需要opencv、skimage库
4. 我使用的模拟器是“网易MuMu模拟器”，若使用其他模拟器请修改程序中寻找窗口部分中的窗口名
5. 程序使用到了图像对比的功能，用于判断当前所处的状态，需要自行预存图片于“initial_IMG/”目录下，不同功能要求存取的图片不同，详见各个功能的README
6. 程序中所有的点击都是在一个矩形区域内随机选点，且点击后有随机的等待间隔，最大程度避免被发现

# 原理概括
基本逻辑和数电里的有限状态机差不多，不断地截取游戏界面并判断所处的状态，然后不同的状态对应于不同的操作。所谓“状态”，就是当前在哪个界面，比如说在主菜单界面，那么状态就是“主菜单”，假如是要自动0-2，那么对应的操作就是点击“作战”；如果在作战选择菜单，那么状态就是“作战选择”，对应的操作就是点击“作战任务”，拖动点击“第零战役”，点击“普通”。

>> 我说得再多再详细也不如自己看看程序，注释我写得比较详细，整体逻辑也比较简单易懂，搞懂了原理你就可以自己改功能了

