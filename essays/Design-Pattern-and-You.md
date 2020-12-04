---
layout: essay
type: essay
title: Design Patterns and you
date: 2020-12-03
labels:
  - Learning
  - Design
  - Pattern
---

# Mostly patterns, some designs

Patterns are abundant and everywhere; sometimes simple and upfront, other time complex and hidden. One could find a pattern in mostly anything and in programing there are plenty. That is not to say it is a bad thing, not everything has to be creative or unique. You still need the fundamentals to make sure the program is stable. Design patterns is an umbrella term for designs that show up frequently that works in a given environment. For example, a house designed in Canada would not work in someplace like Egypt due to the environment being completely different, but it could work in Norway. Similar to programing, there are certain designs that consistently pop up due to it ability to solve problems. There is a brunch of design patterns, the following are just some of the more popular.

 Factory, as its name implies behave similar to a real-life factory, the one the create certain stuffs. One would use a factory when you want to create objects without revealing how it is done and letting the object be molded or have more functions. It is akin to a Coke-Cola factory, there are some secrets that are not shown, and the end product have slight variation a la flavors.
 
A Singleton is an object that is meant to be globally access throughout the program in a language that does not allow global variables. This allows for program to keep track of data from one class to another. How one does it is up to them, most if not all design pattern are concepts that can be adapted as one will. 

The Observer design is for event driven system, or for a reactive system. There are so many examples of this type of design, it is literally everywhere. The best example is the fire alarm system; the fire detector is the observer that will send a message the system and trigger the alarm. 

The model view controller sounds very complicated at first, but it is really just the interaction of the user with the program through a GUI. Every single website you have interact with is a model view controller, the way the data is presented is not the way model is made. By clicking or sometime hovering over something, the view changes allowing the controller more options. 

# Design pattern detected 

Initially I did not understand the idea of design pattern, it is like kind of a are these methods or ideas sort of things. How should I interpret this knowledge. Then something clicked, I have seen these ideas before, I have written a lot of codes that follow these design pattern before even if I did not know about it. Especially the model view controller, I was programing using Visual Studio in one of my previous class. The whole thing about Visual Studio is that there are two side, the visible GUI front side and the messy jumble of code back side. The projects that were assigned had us create the GUI which was basically putting buttons, input fields, and display fields in a sensible manner and then we program function into the buttons, take data from the input, and display whatever it was that need to be done in the display field. 
```
      private void buttonRemoveVehicle_Click(object sender, EventArgs e)
        {
            //if any selection is made in the listbox
            if(listBoxAllVehicles.SelectedIndex > -1)
            {
                //remove from the list first then the lisbox
                vehicleList.RemoveAt(listBoxAllVehicles.SelectedIndex);
                listBoxAllVehicles.Items.RemoveAt(listBoxAllVehicles.SelectedIndex);
               
                if(vehicleList.Count < 1)
                {
                    //if there is no vehicle then both modify and remove button will be disabled
                    buttonModify.Enabled = false;
                    buttonRemoveVehicle.Enabled = false;
                }
            }
            else
            {
                errorProviderInput.SetError(buttonRemoveVehicle, "Please select a vehicle to remove");
            }
        }
```
This code was to make one of the marked button delete a selected item off of the list. In turn this also uses observer design with the error provider at the buttom. It only activate when the user did not select a vehicle and press the button. While this was not something I have done personally, my coworker made a very simple water obsever that sends a email whenever the physical detector sense water

