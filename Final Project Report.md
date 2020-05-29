# OOP 103330:MAZE RUNNER GAME (UNITY)  
### PROJECT MEMBERS:

StdID     |     Name
----------  | -------------
64293     | **Mohsin Amin**
64329     | Shahryar Mukhtar

## Project Description:

As we can guess that this name of project is clearly indicating that it contains a maza and an person is running, his time of acheiving or we can say winning is being recorded.
As we have played and clearly see different games but this maze runner game is quite difficult to be implemented in Visual Studio defining the positions at different points so this was the idea to implement that game in Unity in the 3D.
In this game, A player is trapped inside the maze and he has to find the way out in the given time. He has the controls Arrow key[UP,DOWN,LEFT RIGHT] for movements.
Further, this game consist of 2 levels. You need to trapped out of the maze in the given slot in order to go for another i.e. 2nd level.

## Code:
###Level Changer
public class LevelLoader : MonoBehaviour
{

    public string levelToLoad;

    void OnTriggerEnter(Collider other)
    {
        SceneManager.LoadScene(levelToLoad);
    }

}
###Timer logic
public class Timer : MonoBehaviour
{
    float currentTime = 0f;
    public float startTime;
    public string LevelName;

    public Text CountDownText;
    void Start()
    {
        currentTime = startTime;
    }

    // Update is called once per frame
    void Update()
    {
        if (currentTime > 0)
        {
            currentTime -= 1 * Time.deltaTime;
            print(currentTime);
            CountDownText.text = currentTime.ToString("0");
        }

        if (currentTime >= 3.5f) { CountDownText.color = Color.black; }
        if (currentTime < 3.5f) { CountDownText.color = Color.red; }
        if (currentTime <= 0f) { Application.LoadLevel(LevelName); }

    }
}

##How to Run##
You just need to download the game and install it. It will be ready for you to play.

## Problems Faced

### Problem 1:Game in Unity:
this was the first time we were trying to develop a game in unity so it was quite difficult for us and we took an help from internet(youtube), references are mentioned below.

### Problem 2: New platform and being connected:
Working with social distancing wasn't easy but we did as being a part of student life as it was new to and though we remain in contact through zoom and tried to visit one's home to work in proper and to make over with in a deadline.
Github was also quite tough as we hadnt work before but being a leader and a member we did it we tried our best and this all is the result of efforts of both.

Hope you appreciate us over it!.

## References:
- [refrence link1](https://www.youtube.com/watch?v=pMD0DnOqYnU)
- [refrence link2](https://www.studytonight.com/3d-game-engineering-with-unity/maze-game)
