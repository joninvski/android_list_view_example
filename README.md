[![Build Status](https://travis-ci.org/joninvski/android_list_view_example.svg?branch=master)](https://travis-ci.org/joninvski/android_list_view_example)

Android Basic Fragment Example
==============================

Simple todo application

Introduces the notion of listView, ListActivity and Adapter

<img src="https://github.com/joninvski/android_list_view_example/raw/master/images/todo_list_screenshot.png" alt="todo list screenshot" width="200px;"/>
<img src="https://github.com/joninvski/android_list_view_example/raw/master/images/add_item_screenshot.png" alt="add new todo screenshot" width="200px;"/>

Compile
-------

    # Optional
    ANDROID_HOME=/home/.../android/sdk; export ANDROID_HOME

    ./gradlew compileDebug

Test
----

    # Make sure emulator is running or connected to real device
    ./gradlew connectedInstrumentTest


Code highlights
---------------

Inflate each element in listView:

		LayoutInflater inflater = (LayoutInflater) mContext.getSystemService(Context.LAYOUT_INFLATER_SERVICE);
		View itemLayout = inflater.inflate(R.layout.todo_item, parent, false);		


Add a specific view to the footer of the list

		TextView footerView = null;
		footerView = (TextView) getLayoutInflater().inflate(
				R.layout.footer_view, null);
		this.getListView().addFooterView(footerView);


