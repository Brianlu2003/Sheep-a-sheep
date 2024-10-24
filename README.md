# Sheep-a-sheep
技术文档 类图

classDiagram
    class MainActivity {
        - onCreate()
        - handleCardTap()
    }

    class GameLogic {
        - cardStack: Stack
        - addCardToStack()
        - checkMatch()
        - removeMatchedCards()
    }

    class Card {
        - id: int
        - isVisible: bool
        + getId()
        + setVisible()
    }

    MainActivity --> GameLogic
    GameLogic --> Card

![image](https://github.com/user-attachments/assets/fc78f22d-bbf7-43ba-ae3c-46c989574b9b)

更新类图
```mermaid
classDiagram
    GameActivity --> Timer : 使用计时器
    GameActivity --> GameLogic : 游戏逻辑处理
    GameLogic --> StorageManager : 本地数据存储
    GameActivity --> UIController : 用户界面管理

    class GameActivity {
        +startGame()
        +undoAction()
        +refreshBoard()
    }

    class Timer {
        +start()
        +pause()
        +reset()
    }

    class GameLogic {
        +checkLoop()
        +validateMove()
        +recordHistory()
    }

    class StorageManager {
        +saveTime()
        +loadHistory()
    }

    class UIController {
        +updateUI()
        +showToast()
    }

![SheepGame open](https://github.com/user-attachments/assets/ac97a115-3cb0-45e0-83c1-11c209a90202)



