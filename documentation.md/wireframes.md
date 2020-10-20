## Wireframes

The application consists of three main views. The BikeView with a shortened view of all bikes. The DetailView, a complete view of a selected bike. And the accessory view for tools, spare parts and expendables.

![BikeView](/Users/georgfreitag/Documents/dev/vue/bikeVuer/documentation.md/IMG_C6D78AE3C12D-1.jpeg)

The BikeView (Main View) shows the bikes as a compact summary. Each bike is displayed as a card. It contains information about the manufacturer and model, the year of purchase, a picture and the most important intervals. A new bike can be added using the button at the bottom. 

###### ![DetailView](/Users/georgfreitag/Documents/dev/vue/bikeVuer/documentation.md/IMG_3C0C8997F380-1.jpeg)

The detailed table contains all information about the bike. These are displayed as a simple list. The property name is on the left, the value on the right. Values can be displayed as text, number or interval. Intervals are displayed in a traffic light system. Values within the first two thirds are green, in the last third they turn orange and if there is only 10% remaining time they turn red. 

###### ![Accessoires view](/Users/georgfreitag/Documents/dev/vue/bikeVuer/documentation.md/IMG_7CBBD9ECF4C9-1.jpeg)

In the accessories view, all components are displayed in list form. Each entry contains a name, a description, a quantity and is assigned to a category. Categories are: Consumables, tools and spare parts. To create a new entry, use the plus button in the lower right corner.

![Create a Accessories entry](/Users/georgfreitag/Documents/dev/vue/bikeVuer/documentation.md/IMG_6388797F9FC8-1.jpeg)

An accessory is created in this view. The input is done via a popup, since only a few values have to be entered. 