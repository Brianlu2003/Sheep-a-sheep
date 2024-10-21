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
