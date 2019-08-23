Snake

## controllerl类

```C++
void Start();
void Select();
void DrawGame();
int PlayGame();
void UpdateScore(const int&);
void RewriteScore();
int Menu();
void Game();
int GameOver();
```
## tool类

void SetWindowSize(int cols, int lines);

设置窗口大小和窗口标题

void SetCursorPosition(const int x, const int y);

设置光标位置

void SetColor(int colorID);

设置文本颜色

void SetBackColor();

设置文本背景色



## Point类

基础点类，包括点的输入和坐标转换



## startinterface类

主界面类，负责输出开始动画，分别有蛇的动画(depue)和文字的动画（vector）

蛇通过入队出队来显示蛇的移动。

文字则是X轴集体右移。



## Snake类

```c++
void InitSnake();//初始化蛇的大小和方向，用双端队列，并绘制出来
void Move();//蛇增长，通过判断方向(enum)来入队Point
void NormalMove();//正常移动
bool OverEdge();//判断是否蛇头越界，返回1为否
bool HitItself();//判断是否碰撞到自己的身体，通过复制头部，遍历身体看身体是否与头部重合
bool ChangeDirection();//改变方向
bool GetFood(const Food&);//获取食物
bool GetBigFood(Food&);//获取特殊食物
```
## map类

游戏界面显示，同样是用双端队列



## Food类

```C++
void DrawFood(Snake&);	/*利用rand函数获得坐标，并将其范围限制在2-29内，即在地图内，如果获得的坐标与蛇身重叠，则重新获取。同时每5颗食物就出现一颗限时食物*/
void DrawBigFood(Snake&); //绘制限时食物
void FlashBigFood();//限时食物闪烁
bool GetBigFlag();
int GetProgressBar();
```






































