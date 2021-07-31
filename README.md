## React Inline element input

- This module is basically a text input with some features like tagging people, inserting hash tag, and anythings which can be prefixed with a defined character. For example, it detects '#hashtag' to add a hash tag, '/csome_community_name' to add a community information and '/uusername' to add a user information.

- I analyzed the post editor of FaceBook to implement this module.

- How does it work?
	1) All elements in text input are defined as entities. Each entities have properties - type, location and some required informations.
	2) The core logic - saying CL - converts entities to normal string.
	3) When a character is typed in textarea, CL determines what type the new character is and what intention the user has.
	4) CL uses diff algorithm when it compares previous state and new state.
	5) There is a layer behind textarea. The layer highlights hash tag, tagged user and other elements.
	
- [Usage example](https://github.com/SilverMagnolia/react-inline-element-input/blob/master/src/App.js "Usage example")
	
