Dropdownmenu
============

JAvascrip  dropdown menu 


var menuOpen : boolean; // Whether or not the menu window is open

var menuRect : Rect; // The rectangle for the menu button
var menuWindowRect : Rect; // The rectangle for the menu window

var entryStyle : GUIStyle; // The style for the entries in the menu window

function Start() // This function runs once on object creation
{
  menuRect.x = menuRect.x * Screen.width; // Resize the two rects as a percentage of the screen width and screen height
	menuRect.y = menuRect.y * Screen.height;
	menuRect.width = menuRect.width * Screen.width;
	menuRect.height = menuRect.height * Screen.height;
	menuWindowRect.x = menuWindowRect.x * Screen.width;
	menuWindowRect.y = menuWindowRect.y * Screen.height;
	menuWindowRect.width = menuWindowRect.width * Screen.width;
	menuWindowRect.height = menuWindowRect.height * Screen.height;
}

function OnGUI() // This function runs multiple times per frame
{
	GUI.Button(menuRect, "Test Menu"); // Create the menu button
	if (menuOpen) { // If the menu is open
		GUI.Window(2, menuWindowRect, WindowFunc, ""); // Create the menu window
	}
}

function Update() // This function runs once a frame
{
	if (Input.GetMouseButtonDown(0)) { // If the user presses the left mouse button
		if (Input.mousePosition.x > menuRect.x && Input.mousePosition.x < menuRect.x + menuRect.width && Screen.height - Input.mousePosition.y > menuRect.y && Screen.height - Input.mousePosition.y < menuRect.y + menuRect.height) { // If the mouse is currently inside the button rect
			menuOpen = !menuOpen; // Open or close the menu
		}
	}
	if (menuOpen) { // If the menu is open
		if (Input.mousePosition.x < menuRect.x || Input.mousePosition.x > menuRect.x + menuRect.width || Screen.height - Input.mousePosition.y < menuRect.y || Screen.height - Input.mousePosition.y > menuRect.y + menuRect.height + menuWindowRect.height) { // If the mouse position is outside the window or menu
			menuOpen = false; // Close the menu
		}
	}
	if (Input.GetMouseButtonUp(0)) { // If the user lets up the mouse button
		if (Input.mousePosition.x > menuWindowRect.x && Input.mousePosition.x < menuWindowRect.x + menuWindowRect.width && Screen.height - Input.mousePosition.y > menuWindowRect.y && Screen.height - Input.mousePosition.y < menuWindowRect.y + menuWindowRect.height * .25) { // If the mouse is over the new file button
			Debug.Log("New File Up"); // Print out a debug message
		}
		if (Input.mousePosition.x > menuWindowRect.x && Input.mousePosition.x < menuWindowRect.x + menuWindowRect.width && Screen.height - Input.mousePosition.y > menuWindowRect.y  + menuWindowRect.height * .25 && Screen.height - Input.mousePosition.y < menuWindowRect.y + menuWindowRect.height * .5) { // If the mouse is over the load file button
			Debug.Log("Load File Up"); // Print out a debug message
		}
		if (Input.mousePosition.x > menuWindowRect.x && Input.mousePosition.x < menuWindowRect.x + menuWindowRect.width && Screen.height - Input.mousePosition.y > menuWindowRect.y  + menuWindowRect.height * .5 && Screen.height - Input.mousePosition.y < menuWindowRect.y + menuWindowRect.height * .75) { // If the mouse is over the save file button
			Debug.Log("Save File Up"); // Print out a debug message
		}
		if (Input.mousePosition.x > menuWindowRect.x && Input.mousePosition.x < menuWindowRect.x + menuWindowRect.width && Screen.height - Input.mousePosition.y > menuWindowRect.y  + menuWindowRect.height * .75 && Screen.height - Input.mousePosition.y < menuWindowRect.y + menuWindowRect.height) { // If the mouse is over the quit button
			Debug.Log("Quit Up"); // Print out a debug message
		}
	}
}

function WindowFunc(windowID : int) // This function controls the contents of the window that calls the function
{
	if (GUI.Button(Rect(0, 0, menuWindowRect.width, menuWindowRect.height * .25), "New File", entryStyle)) { // If the user clicks the new file button
		Debug.Log("New File Click"); // Print a debug message
	}
	if (GUI.Button(Rect(0, menuWindowRect.height * .25, menuWindowRect.width, menuWindowRect.height * .25), "Load File", entryStyle)) { // If the user clicks the load file button
		Debug.Log("Load File Click"); // Print a debug message
	}
	if (GUI.Button(Rect(0, menuWindowRect.height * .5, menuWindowRect.width, menuWindowRect.height * .25), "Save File", entryStyle)) { // If the user clicks the save file button
		Debug.Log("Save File Click"); // Print a debug message
	}
	if (GUI.Button(Rect(0, menuWindowRect.height * .75, menuWindowRect.width, menuWindowRect.height * .25), "Quit", entryStyle)) { // If the user clicks the quit button
		Debug.Log("Quit Click"); // Print a debug message
	}
}
