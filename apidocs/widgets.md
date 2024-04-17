# Notes for module dflib.widgets
## function dflib.widgets._widget_set_css(widget, classname, css_data)
Apply classname and css_data to arbitrary widget
	

## `class dflib.widgets.MessageDialog`
Ths class implments a MessageBox as a Gtk.Window

	Constructor parameters:
		buttons: list of strings to be placed on buttons (ok, cancel etc) default: ["OK"]
		callback: function to run if button is pressed. The str label of the button is passed
		icon: name of icon to use, eother Gtk.ICON_xxx or a filename. Default is Gtk.ICON_DIALOG_INFO
		message: message to show
		parent: if set the window becomes modal and transient for the parent. 
		title: title of window

		Callback is option and if not set, clicking a button destroys the dialog. 
		Title and message must be set.
	

## `class dflib.widgets.AboutDialog`
 Display an AboutDialog implemented as a MessageDialog

		kwargs:
			title - window title
			message - message to display
			parent - parent widget, if set dialog is modal
			icon - name or path of icon 
			buttons - list of buttons to show
	

## `class dflib.widgets.Toggle`
Toggle is a control that has a label either above or to the left of the toggle button. 

	kwargs:
		label_text - a list of two strings to show on the button  for toggled or not
		orientation - should be a Gtk.Orientation type
		caption - label to show next to or above button
		state - boolean initial state
		callback - function to call on state change, receives button label text
	

### `class dflib.widgets.ListBox`
Simplified interface for a GtkListBos

	keyword arguments:
		onSelect: activated when a row is selected, callback receives label text
		onActivate: activated when a row is activated (double clicked) same as above
	

### `dflib.widgets.ListBox.select_row_by_label(self,text)`
set the row with that has the label in text
		

### `dflib.widgets.ListBox.remove_row_by_label(self,label)`
remove a row by the row's label
		

### `dflib.widgets.ListBox.populate(self,items)`
Clear and reload the ListBox with items
		

### `dflib.widgets.ListBox.on_row_activated(self,widget,data)`
Event handler to be activated by row activation. If there is a callback supplied by the 
caller, the clalback is made.
		

### `dflib.widgets.ListBox.on_row_selected(self,widget,data)`
Event handler to be activated when row is selected. Call the supplied callback with the label
		

### dflib.widgets.ListBox.get_selected_item(self):
Get current selected row 

## `class dflib.widgets.LabeledEntry`
LabeledEntry is a control that has a label either above or to the left of an entry field.

	__init__ kwargs:
		text - text to load in the entry field
		orientation - should be a Gtk.Orientation type
		caption - label to show next to or above button
		callback - function to call on entry change
	

## `class dflib.widgets.Button`
wrapper for gtk.Button

	kwargs:
		style: css styles to use
		css_class: css class name to use
		name: name of widget
		icon_name Gtk icon name to use
		label = label text to use (markup ok)
		relief: wheter to use Gtk relief on the button
	

## `class dflib.widgets.MenuBar`
Dictionary driven menu_bar

	MenuBar creates a set of menus based on the dictionary menu_items. 
	it is organized as A dict of menu bar entry, list of entry items. Each
	entry item consists of a caption and an action. See example below. 

		menu_items = {
			"File": [
				{"caption": "About", "action": self.handler},
				{"caption": "---", "action": self.handler},
				{"caption": "Open", "action": self.handler},
				{"caption": "Save As","action": self.handler},
				{"caption": "---", "action": self.handler},
				{"caption": "Quit", "action": self.handler},
			], 
			"Configuration": [
				{"caption": "Configuation Editor", "action": self.handler},
			]
		}


	
