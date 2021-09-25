How to make IconWin in KadeEngine (Ver 1.5.4)
Need
1.Visual Studio Code 2017 or 2019
2.IconGird with normal death win
If you doesn't have IconGird with normal death win download this!
![iconGrid](https://user-images.githubusercontent.com/82280216/134770476-d54b272d-f1d0-404c-b7b0-694e9332a961.png)

1. Go to HealthIcon.hx
![image](https://user-images.githubusercontent.com/82280216/134769393-4a1d13af-416b-4ae4-ad06-dac9182906ed.png)
2.ctrl + f animation.add('bf-car', [0, 1], 0, false, isPlayer);
beetween [Number, Number] is Number Icon exemple
![image](https://user-images.githubusercontent.com/82280216/134769562-ae683891-e0fa-49e8-b580-86d8c4a655fd.png)
If you want add New Icon Count from 43
3.beetween [Number, Number, Number] I will enter the number that [0, 1, 2]
![image](https://user-images.githubusercontent.com/82280216/134769785-3999e919-2690-47b2-8bf2-b33f7bb1c7bb.png)
and ctrl + s to save
4.Go to PlayState.hx
![image](https://user-images.githubusercontent.com/82280216/134769856-adafd431-70d5-4e33-b123-33bfbedbac28.png)
and ctrl + f  if (health > 2)
Usually it will be like this.

                if (healthBar.percent < 20)
		    iconP1.animation.curAnim.curFrame = 1;
		else
		    iconP1.animation.curAnim.curFrame = 0;

		if (healthBar.percent > 80)
		    iconP2.animation.curAnim.curFrame = 1;
		else
		    iconP2.animation.curAnim.curFrame = 0;

![image](https://user-images.githubusercontent.com/82280216/134770332-6acd0226-4042-4cde-b6d3-9ecf4c06e63d.png)
      
To be like this

                if (healthBar.percent < 20)
	            iconP1.animation.curAnim.curFrame = 1;
		else if (healthBar.percent > 80)
		    iconP1.animation.curAnim.curFrame = 2;
		else
		    iconP1.animation.curAnim.curFrame = 0;

		if (healthBar.percent > 80)
	            iconP2.animation.curAnim.curFrame = 1;
		else if (healthBar.percent < 20)
	            iconP2.animation.curAnim.curFrame = 2;
		else
		    iconP2.animation.curAnim.curFrame = 0;
		    
![image](https://user-images.githubusercontent.com/82280216/134770374-e91903f3-786d-47d8-a4cb-beac4e515d06.png)

5. Run game With
		
	 	Lime test windows

