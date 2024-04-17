# Notes for module dflib.widgets
## _widget_set_css


	this function takes an arbitrary widget and applies the classname as it's class
	the css_data is applied to the widget.
	

## MessageDialog


	MessageDialog
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
	

## AboutDialog

 Display an AboutDialog implemented as a MessageDialog
		kwargs:
			title - window title
			message - message to display
			parent - parent widget, if set dialog is modal
			icon - name or path of icon 
			buttons - list of buttons to show
	

## Toggle


	Toggle is a control that has a label either above or to the left of the 
	toggle button. 

	kwargs:
		label_text - a list of two strings to show on the button  for toggled or not
		orientation - should be a Gtk.Orientation type
		caption - label to show next to or above button
		state - boolean initial state
		callback - function to call on state change, receives button label text
	

## ListBox

 Simplified interface for a GtkListBos
	keyword arguments:
		onSelect: activated when a row is selected, callback receives label text
		onActivate: activated when a row is activated (double clicked) same as above
	

## LabeledEntry


	LabeledEntry is a control that has a label either above or to the left of an
	entry field.

	__init__ kwargs:
		text - text to load in the entry field
		orientation - should be a Gtk.Orientation type
		caption - label to show next to or above button
		callback - function to call on entry change
	

## Button


	wrapper for gtk.Button
	kwargs:
		style: css styles to use
		css_class: css class name to use
		name: name of widget
		icon_name Gtk icon name to use
		label = label text to use (markup ok)
		relief: wheter to use Gtk relief on the button
	

## MenuBar


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


	

## select_row_by_label


		set the row with that has the label in text
		

## remove_row_by_label


		remove a row by the row's label
		

## populate


		Clear and reload the ListBox with items
		

## on_row_activated


		callack when row is activated. Call the supplied callback with the label
		

## on_row_selected


		callack when row is selected. Call the supplied callback with the label
		

## get_selected_item

 get current selected row 


