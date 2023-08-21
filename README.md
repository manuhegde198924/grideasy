# grideasy
screen shots of pdf:
https://github.com/manuhegde198924/grideasy/issues/1#issue-1858778367
html is divided into a min part with div and an image and paragraphs
css part
Transitions in CSS allow us to control the way in which transition takes place between the two states of the element. For example, when hovering your mouse over a button, you can change the background color of the element with help of CSS selector and pseudo-class. We can change any other or combination of properties, though. The transition allows us to determine how the change in color takes place. We can use the transitions to animate the changes and make the changes visually appealing to the user and hence, giving a better user experience and interactivity. In this article, we will show you how to animate the transition between the CSS properties. There are four CSS properties that you should use, all or in part (at least two, transition-property and transition-duration, is a must), to animate the transition. All these properties must be placed along with other CSS properties of the initial state of the element:

1. transition-property: This property allows you to select the CSS properties which you want to animate during the transition(change). 

Syntax:

transition-property: none | all | property | property1,
property2, ..., propertyN;

    Values:
        none is used to specify that no property should be selected.
        all is used to specify all the properties to be selected, though not all properties are animate-able, only the properties which are animate-able will be influenced.
        We can specify a single property or a set of comma-separated properties property1, property2, …, propertyN.

2. transition-duration: This property allows you to determine how long it will take to complete the transition from one CSS property to the other. 

Syntax:

transition-duration: time;

    Here, time can be in seconds(s) or milliseconds(ms), you should use ‘s’ or ‘ms’ after the number (without quotes).

3. transition-timing-function: This property allows you to determine the speed of change and the manner of change, during the transition. Like, the change should be fast at the beginning and slow at the end, etc. 

Syntax:

transition-timing-function: ease|ease-in|ease-out|ease-in-out|linear|
step-start|step-end;

    Note, there are other values that this transition-timing-function can take, only the most frequent and simple are mentioned here.

4. transition-delay: This property allows you to determine the amount of time to wait before the transition actually starts to take place. 

Syntax:

transition-delay: time;

    Here, again, time can be in seconds(s) or milliseconds(ms), and you should use ‘s’ or ‘ms’ after the number (without quotes).

The Shorthand Property You can combine all the four transition properties mentioned above, into one single shorthand property, according to the syntax given below. This saves us from writing long codes and prevents from getting messy. Note the ordering of property, it has significance. 

Syntax:

transition: (property name) | (duration) | (timing function) | (delay);

The value is taken by are same as mentioned above. This property must be placed with other CSS properties, if any, of the initial state. You should use at least, property name and duration to get any animate-able effect. Also, the ordering of the values matters. The first value is of the property name, second for the duration and so on, as listed above. So, if only one number is mentioned, it will be taken up as duration, and not as a delay. 

Example: Changing property without using transitions. 

<!DOCTYPE html>
<html>
<head>
    <title>CSS Transition</title>
 
    <style>
        h1 {
            color: green;
            text-align: center;
        }
 
        div.one {
            height: 150px;
            width: 150px;
            border: 1px dashed black;
            margin: 0 auto;
            background: #FFEBEE;
        }
 
        div.one:hover {
            height: 300px;
            width: 300px;
            background: #BBDEFB;
        }
    </style>
 
</head>
 
<body>
    <h1>GeeksForGeeks</h1>
 
    <div class="one">
    </div>
 
</body>
</html>

Output:

 change-without-transition 

Example: Changing property using transitions. 

<!DOCTYPE html>
<html>
<head>
    <title>CSS Transition</title>
 
    <style>
        h1 {
            color: green;
            text-align: center;
        }
 
        div.one {
            height: 150px;
            width: 150px;
            border: 1px dashed black;
            margin: 0 auto;
            background: #FFEBEE;
            transition: height 2s, width 2s, background 2s;
        }
 
        div.one:hover {
            height: 300px;
            width: 300px;
            background: #BBDEFB;
        }
    </style>
 
</head>
 
<body>
    <h1>GeeksForGeeks</h1>
    <div class="one">
    </div>
 
</body>
</html>
CSS Animation: CSS Animations is a technique to change the appearance and behavior of various elements in web pages. It is used to control the elements by changing their motions or display. It has two parts, one contains the CSS properties which describe the animation of the elements and the other contains certain keyframes which indicate the animation properties of the element and the specific time intervals at which those have to occur. 
What is a Keyframe?

Keyframes are the foundations with the help of which CSS Animations work. They define the display of the animation at the respective stages of its whole duration. For example: In the first example code, the paragraph changes its color with time. At 0% completion, it is red, at 50% completion it is of orange color and at full completion i.e. at 100%, it is brown. 
Syntax:

/*property-name*/: /*value*/;

Animation Properties:

There are certain animation properties given below:

    animation-name: It is used to specify the name of the @keyframes describing the animation.
    animation-duration: It is used to specify the time duration it takes animation to complete one cycle.
    animation-timing-function: It specifies how animations make transitions through keyframes. There are several presets available in CSS which are used as the value for the animation-timing-function like linear, ease,ease-in,ease-out, and ease-in-out. 
    animation-delay: It specifies the delay of the start of an animation.
    animation-iteration-count: This specifies the number of times the animation will be repeated.
    animation-direction: It defines the direction of the animation. animation direction can be normal, reverse, alternate, and alternate-reverse.
    animation-fill-mode: It defines how styles are applied before and after animation. The animation fill mode can be none, forwards, backwards, or both.
    animation-play-state: This property specifies whether the animation is running or paused.

Example 1: This example describes the CSS Animation using the @keyframe rule.

<!DOCTYPE html>
<html>
<head>
    <style>
        #gfg {
            animation-name: color;
            animation-duration: 25s;
            padding-top: 30px;
            padding-bottom: 30px;
            font-family: Times New Roman;
        }
 
        #geeks {
            font-size: 40px;
            text-align: center;
            font-weight: bold;
            color: #090;
            padding-bottom: 5px;
        }
 
        #geeks1 {
            font-size: 17px;
            font-weight: bold;
            text-align: center;
        }
 
        @keyframes color {
            0% {
                background-color: red;
            }
 
            50% {
                background-color: orange;
            }
 
            100% {
                background-color: brown;
            }
        }
    </style>
</head>
 
<body>
    <div id="gfg">
        <div id="geeks">GeeksforGeeks</div>
        <div id="geeks1">A computer science portal for geeks</div>
    </div>
</body>
</html>

Output:

Example 2: This example describes the CSS Animation Properties using the animation-duration property.

<html>
<head>
    <style>
        #gfg1 {
            animation-name: text;
            animation-duration: 5s;
            animation-iteration-count: infinite;
        }
 
        #geek1 {
            font-size: 40px;
            text-align: center;
            font-weight: bold;
            color: #090;
            padding-bottom: 5px;
        }
 
        #geek2 {
            font-size: 17px;
            font-weight: bold;
            text-align: center;
        }
 
        @keyframes text {
            from {
                margin-top: 400px;
            }
 
            to {
                margin-top: 0px;
            }
        }
    </style>
</head>
 
<body>
    <div id="gfg1">
        <div id="geek1">GeeksforGeeks</div>
        <div id="geek2">A computer science portal for geeks</div>
    </div>
</body>
</html>

Output: The animation will look like this:

Example 3: This example describes the CSS Animation Properties using the animation-timing-function property.

<!DOCTYPE html>
<html>
<head>
    <style>
        .geeks {
            font-size: 40px;
            text-align: center;
            font-weight: bold;
            color: #090;
            padding-bottom: 5px;
            font-family: Times New Roman;
        }
 
        .geeks1 {
            font-size: 17px;
            font-weight: bold;
            text-align: center;
            font-family: Times New Roman;
        }
 
        h2 {
            width: 350px;
            animation-name: text;
            animation-duration: 4s;
            animation-iteration-count: infinite;
            background-color: rgb(255, 210, 85);
        }
 
        #one {
            animation-timing-function: ease;
        }
 
        #two {
            animation-timing-function: linear;
        }
 
        #three {
            animation-timing-function: ease-in;
        }
 
        #four {
            animation-timing-function: ease-out;
        }
 
        #five {
            animation-timing-function: ease-in-out;
        }
 
        @keyframes text {
            from {
                margin-left: 60%;
            }
 
            to {
                margin-left: 0%;
            }
        }
    </style>
</head>
 
<body>
    <div class="geeks">GeeksforGeeks</div>
    <div class="geeks1">A computer science portal for geeks</div>
    <h2 id="one">This text is ease.</h2>
    <h2 id="two">This text is linear.</h2>
    <h2 id="three">This text is ease-in.</h2>
    <h2 id="four">This text is ease-out.</h2>
    <h2 id="five">This text is ease-in-out.</h2>
</body>
</html>

Output:

Example 4: This example describes the CSS Animation Properties using the animation-delay property.

<!DOCTYPE html>
<html>
<head>
    <style>
        .geeks {
            font-size: 40px;
            text-align: center;
            font-weight: bold;
            color: #090;
            padding-bottom: 5px;
            font-family: Times New Roman;
        }
 
        .geeks1 {
            font-size: 17px;
            font-weight: bold;
            text-align: center;
            font-family: Times New Roman;
        }
 
        #one {
            animation-name: example;
            animation-duration: 10s;
        }
 
        #two {
            animation-name: example;
            animation-duration: 10s;
            animation-delay: 10s;
        }
 
        @keyframes example {
            from {
                background-color: orange;
            }
 
            to {
                background-color: white;
            }
        }
    </style>
</head>
 
<body>
    <div class="geeks">GeeksforGeeks</div>
    <div class="geeks1">A computer science portal for geeks</div>
    <h2 id="one">Text animation without delayed.</h2>
    <h2 id="two">Text animation with 10 second delay.</h2>
</body>
</html>

Output:

Example 5: This example describes the CSS Animation Properties using an animation-iteration-count property.

<!DOCTYPE html>
<html>
<head>
    <style>
        .geeks {
            font-size: 40px;
            text-align: center;
            font-weight: bold;
            color: #090;
            padding-bottom: 5px;
            font-family: Times New Roman;
        }
 
        .geeks1 {
            font-size: 17px;
            font-weight: bold;
            text-align: center;
            font-family: Times New Roman;
        }
 
        #one {
            animation-name: example;
            animation-duration: 2s;
            animation-iteration-count: 2;
        }
 
        #two {
            animation-name: example;
            animation-duration: 2s;
            animation-iteration-count: infinite;
        }
 
        @keyframes example {
            from {
                background-color: orange;
            }
 
            to {
                background-color: white;
            }
        }
    </style>
</head>
 
<body>
    <div class="geeks">GeeksforGeeks</div>
    <div class="geeks1">A computer science portal for geeks</div>
    <h2 id="one">This text changes its color two times.</h2>
    <h2 id="two">This text changes its color infinite times.</h2>
</body>
</html>

Output:

Example 6: This example describes the CSS Animation Properties using the animation-direction property.

<!DOCTYPE html>
<html>
<head>
    <style>
        .geeks {
            font-size: 40px;
            text-align: center;
            font-weight: bold;
            color: #090;
            padding-bottom: 5px;
            font-family: Times New Roman;
        }
 
        .geeks1 {
            font-size: 17px;
            font-weight: bold;
            text-align: center;
            font-family: Times New Roman;
        }
 
        h2 {
            width: 100%;
            animation-name: text;
            animation-duration: 2s;
            animation-iteration-count: infinite;
        }
 
        #one {
            animation-direction: normal;
        }
 
        #two {
            animation-direction: reverse;
        }
 
        #three {
            animation-direction: alternate;
        }
 
        #four {
            animation-direction: alternate-reverse;
        }
 
        @keyframes text {
            from {
                margin-left: 60%;
            }
 
            to {
                margin-left: 0%;
            }
        }
    </style>
</head>
 
<body>
    <div class="geeks">GeeksforGeeks</div>
    <div class="geeks1">A computer science portal for geeks</div>
    <h2 id="one">This text is normal.</h2>
    <h2 id="two">This text is reverse.</h2>
    <h2 id="three">This text is alternate.</h2>
    <h2 id="four">This text is alternate-reverse.</h2>
</body>
</html>

Output:

Example 7: This example describes the CSS Animation Properties using an animation-fill-mode property.

<!DOCTYPE html>
<html>
<head>
    <style>
        .geeks {
            font-size: 40px;
            text-align: center;
            font-weight: bold;
            color: #090;
            padding-bottom: 5px;
            font-family: Times New Roman;
        }
 
        .geeks1 {
            font-size: 17px;
            font-weight: bold;
            text-align: center;
            font-family: Times New Roman;
        }
 
        h2 {
            width: 400px;
            background-color: orange;
            animation-name: text;
            animation-duration: 3s;
        }
 
        #one {
            animation-fill-mode: none;
        }
 
        #two {
            animation-fill-mode: forwards;
        }
 
        #three {
            animation-fill-mode: backwards;
            animation-delay: 2s;
        }
 
        #four {
            animation-fill-mode: both;
            animation-delay: 2s;
        }
 
        @keyframes text {
            from {
                margin-left: 0%;
                background-color: #aaaaaa;
            }
 
            to {
                margin-left: 60%;
                background-color: #008000;
            }
        }
    </style>
</head>
 
<body>
    <div class="geeks">GeeksforGeeks</div>
    <div class="geeks1">A computer science portal for geeks</div>
    <h2 id="one">none</h2>
    <h2 id="two">forwards</h2>
    <h2 id="three">backwards</h2>
    <h2 id="four">both</h2>
</body>
</html>

Output:

Animation Shorthand Property: It is a shorthand way of implying the animation properties for a quicker code. The properties should be in the following order:

animation: [animation-name] [animation-duration] [animation-timing-function] [animation-delay] 
           [animation-iteration-count] [animation-direction] [animation-fill-mode] 
           [animation-play-state];

For example, normally the animation code would be like this:

Example 8: This example describes the CSS Animation Properties using an animation-play-state property, without an animation shorthand property.

<!DOCTYPE html>
<html>
<head>
    <style>
        #g4g {
            width: 400px;
            height: 100px;
            position: relative;
            animation-name: GFG;
            animation-duration: 5s;
            animation-timing-function: linear;
            animation-delay: 1s;
            animation-iteration-count: infinite;
            animation-direction: alternate;
        }
 
        @keyframes GFG {
            0% {
                left: 0px;
                top: 0px;
            }
 
            25% {
                left: 200px;
                top: 200px;
            }
 
            50% {
                left: 200px;
                top: 0px;
            }
 
            75% {
                left: 0px;
                top: 200px;
            }
 
            100% {
                left: 0px;
                top: 0px;
            }
        }
    </style>
</head>
 
<body>
    <img id="g4g" src=
"https://media.geeksforgeeks.org/wp-content/cdn-uploads/GeeksforGeeksLogoHeader.png" />
</body>
</html>

Output:

In shorthand, the above HTML code can be written as:

Example 9: This example describes the CSS Animation Properties using an animation-play-state property, with an animation shorthand property.

<!DOCTYPE html>
<html>
<head>
    <style>
        #geeks4g {
            width: 400px;
            height: 100px;
            position: relative;
            animation: GFG 5s linear 1s infinite alternate;
        }
 
        @keyframes GFG {
            0% {
                left: 0px;
                top: 0px;
            }
 
            25% {
                left: 200px;
                top: 200px;
            }
 
            50% {
                left: 200px;
                top: 0px;
            }
 
            75% {
                left: 0px;
                top: 200px;
            }
 
            100% {
                left: 0px;
                top: 0px;
            }
        }
    </style>
</head>
 
<body>
    <img id="geeks4g" src=
"https://media.geeksforgeeks.org/wp-content/cdn-uploads/GeeksforGeeksLogoHeader.png" />
</body>
</html>
The Media query in CSS is used to create a responsive web design. It means that the view of a web page differs from system to system based on screen or media types. The breakpoint specifies for what device-width size, the content is just starting to break or deform.

Media queries can be used to check many things:

    width and height of the viewport
    width and height of the device
    Orientation
    Resolution

A media query consist of a media type that can contain one or more expression which can be either true or false. The result of the query is true if the specified media matches the type of device the document is displayed on. If the media query is true then a style sheet is applied.

Syntax:

@media not | only mediatype and (expression) {
    // Code content
}

Example: This example illustrates the CSS media query with the different device-width for making it responsive.

<!DOCTYPE html>
<html>
 
<head>
    <title>CSS media query</title>
    <style>
        body {
            text-align: center;
        }
 
        .gfg {
            font-size: 40px;
            font-weight: bold;
            color: green;
        }
 
        @media screen and (max-width:800px) {
            body {
                text-align: center;
                background-color: green;
            }
 
            .gfg {
                font-size: 30px;
                font-weight: bold;
                color: white;
            }
 
            .geeks {
                color: white;
            }
        }
 
        @media screen and (max-width:500px) {
            body {
                text-align: center;
                background-color: blue;
            }
        }
    </style>
</head>
 
<body>
    <div class="gfg">
        GeeksforGeeks
    </div>
    <div class="geeks">
        A computer science portal for geeks
    </div>
</body>
 
</html>

Output: From the output, we can see that if the max-width of the screen is reduced to 800px then the background color changes to green & if the max-width of the screen is reduced to 500px then the background color will turn to blue. For the desktop size width, the background color will be white.

Media Types in CSS: There are many types of media types which are listed below:

    all: It is used for all media devices
    print: It is used for printer.
    screen: It is used for computer screens, smartphones, etc.
    speech: It is used for screen readers that read the screen aloud.

Features of Media query: There are many features of media query which are listed below:

    color: The number of bits per color component for the output device.
    grid: Checks whether the device is grid or bitmap.
    height: The viewport height.
    aspect ratio: The ratio between width and height of the viewport.
    color-index: The number of colors the device can display.
    max-resolution: The maximum resolution of the device using dpi and dpcm.
    monochrome: The number of bits per color on a monochrome device.
    scan: The scanning of output devices.
    update: How quickly can the output device modify.
    width: The viewport width.
The opacity in CSS is the property of an element that describes the transparency of the element. It is the opposite of transparency & represents the degree to which the content will be hidden behind an element.

We can apply the opacity with different styling properties to the elements. A few of them are discussed below:

Image Opacity: The opacity property is used in the image to describe the transparency of the image. The value of opacity lies between 0.0 to 1.0 where a low value represents high transparency and a high value represents low transparency. The percentage of opacity is calculated as Opacity% = Opacity * 100.

Example: This example describes the opacity property by applying it to the image.

<!DOCTYPE html>
<html>
 
<head>
    <title>Opacity property</title>
    <style>
        .forest {
            opacity: 0.5;
        }
 
        p {
            font-size: 25px;
            font-weight: bold;
            margin-bottom: 5px;
        }
 
        .opacity {
            text-align: center;
        }
    </style>
</head>
 
<body>
    <div class="opacity">
 
        <p>Image with 100% opacity (original image)</p>
 
        <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-10.png"
             class="forest1">
        <br>
        <br>
 
        <p>Image with 50% opacity</p>
 
        <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-10.png"
             class="forest">
    </div>
</body>
 
</html>

Output:

image opacity

Image Hover Opacity: The hover opacity property is applied to the image when the mouse puts it over the image otherwise opacity property changes. The value of opacity can easily reverse the process by setting the opacity as a higher value at first and then lowering it when hovering over it like:

Syntax:

.hightolow {
    opacity: 1.0;
}
.hightolow:hover {
    opacity: 0.5;
}

Example: This example describes the opacity property by applying it to the image to generate opacity by hovering over it.

<!DOCTYPE html>
<html>
 
<head>
    <title>Image Hover Opacity</title>
    <style>
        .gfg_opacity {
            opacity: 0.5;
        }
 
        .gfg_opacity:hover {
            opacity: 1.0;
        }
 
        .main {
            text-align: center;
        }
    </style>
</head>
 
<body>
    <div class="main">
        <h1>Image Hover Opacity:</h1>
        <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-10.png"
             class="gfg_opacity">
        <br>
        <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-10.png"
             class="gfg_opacity">
        <br>
        <br>
    </div>
</body>
 
</html>

Output:

hover image opacity

Transparency box and transparency using RGBA values: In the transparency box, the child property inherit the property from the parent property but in the case of transparency using RGBA, only the opacity property is used or applied to add transparency to the background of an element.

Example: This example describes the opacity property by applying transparency using RGBA values.

<!DOCTYPE html>
<html>
 
<head>
    <title>Transparent box</title>
    <style>
        .geeks {
            background: rgb(0, 153, 0);
            padding: 15px;
            text-align: center;
            width: 300px;
        }
 
        #geek {
            padding: 15px;
            text-align: center;
            width: 300px;
        }
 
        .rgba1 {
            background: rgba(0, 153, 0, 0.1);
        }
 
        .rgba2 {
            background: rgba(0, 153, 0, 0.5);
        }
 
        .rgba3 {
            background: rgba(0, 153, 0, 0.8);
        }
 
        .rgba4 {
            background: rgba(0, 153, 0, 1.0);
        }
 
        .g1 {
            float: left;
            margin-left: 50px;
        }
 
        .g2 {
            margin-top: -40px;
            margin-left: 50px;
            float: left;
        }
    </style>
</head>
 
<body>
    <div class="g1">
        <p style="font-size:24px;font-weight:bold;">
            Transparent Box
        </p>
 
        <div class="geeks" style="opacity:0.1;">
 
            <p>10% opacity</p>
 
        </div>
        <div class="geeks" style="opacity:0.5;">
 
            <p>50% opacity</p>
 
        </div>
        <div class="geeks" style="opacity:0.8;">
 
            <p>80% opacity</p>
 
        </div>
        <div class="geeks">
 
            <p>100% opacity</p>
 
        </div>
    </div>
    <br>
    <br>
    <div class="g2">
        <p style="font-size:24px;font-weight:bold;">
            RGBA color values
        </p>
 
        <div class="rgba1" id="geek">
            <p>10% opacity</p>
 
        </div>
        <div class="rgba2" id="geek">
            <p>50% opacity</p>
 
        </div>
        <div class="rgba3" id="geek">
            <p>80% opacity</p>
 
        </div>
        <div class="rgba4" id="geek">
            <p>100% opacity</p>
 
        </div>
    </div>
</body>
 
</html>

Output:

opacity

Text In Transparent Box: The “Text in Transparent Box” property is a concept where the background of a box is made transparent while keeping the text inside the box fully visible and opaque. This effect is achieved by adjusting the opacity or transparency of the background color while leaving the text unaffected.

Example: This example describes the opacity property by placing the text in a transparent box.

<!DOCTYPE html>
<html>
<head>
    <style>
        div.bg {
background:url("https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-10.png");
            width: 550px;
            height: 300px;
            border: 1px solid;
        }
 
        div.box {
            margin: 50px 20px;
            text-align: center;
            width: 500px;
            height: 150px;
            background-color: rgba(0, 0, 0, 0.7); /* Transparent background color */
            border: 3px solid white;
        }
 
        div.box p {
            margin: 5%;
            font-family: Arial;
            color: #009900;
            font-weight: bold;
            font-size: 25px;
        }
    </style>
</head>
<body>
    <div class="bg">
        <div class="box">
            <p>GeeksforGeeks</p>
        </div>
    </div>
</body>
</html>
The CSS grid layout module is used to create a grid-based layout system, with the help of rows and columns it makes it easier to design any webpage without using floats and positioning.

Syntax:

.class {
    display:grid;
}

Note: An HTML element becomes a grid if that element sets display: grid; in style section or inline-grid. Below you will see both examples.

CSS Grid Layout Properties: These are the following grid-layout properties:

    column-gap: It is used to specify the amount of gap between the columns in which a given text is divided using the column-count property.
    gap: It is used to set the spacing also caller gutter between the rows and columns.
    grid: It offers a grid-based layout system, with rows and columns, making it easier to design web pages without floats and positioning.
    grid-area: It is used to set a grid item size and location in a grid layout.
    grid-auto-columns: It is used to specify the size for the columns of implicitly generated grid containers.
    grid-auto-flow: It specifies exactly how auto-placed items get flow into the grid.
    grid-auto-rows: It is used to specify the size for the rows of implicitly generated grid containers.
    grid-column: It describes the number of properties that allow to design of grid structures and control the placement of grid items using CSS.
    grid-column-end: It explains the number of columns an item will span, or on which column-line the item will end.
    grid-column-gap: It is used to set the size of the gap between the columns in a grid layout.
    grid-column-start: It defines for which column line item will start.
    grid-gap: It is used to sets the size of the gap between the rows and columns in a grid layout.
    grid-row: It is used to specify the size and location in a grid layout.
    grid-row-end: It is used to define the grid item’s end position within a grid row by specifying the inline edge of its grid area.
    grid-row-gap: It is used to define the size of the gap between the grid elements.
    grid-row-start: It is used to define the grid items’ start position within the grid row by specifying the inline start edge of its grid area.
    grid-template: It is a shorthand property for defining grid columns, rows, and areas.
    grid-template-areas: It is used to specify the area within the grid layout.
    grid-template-columns: It is used to set the number of columns and size of the columns of the grid.
    grid-template-rows: It is used to set the number of rows and height of the rows in a grid.

Example 1: This example illustrates the use of display: grid; property.

<!DOCTYPE html>
<html>
 
<head>
    <style>
        /* Designing all grid */
        .grid-container {
            display: grid;
            grid-template-columns: auto auto auto;
            background-color: gray;
            padding: 5px;
        }
 
        /* Designing all grid-items */
        .grid-item {
            background-color: rgba(255, 255, 255, 0.8);
            border: 1px solid black;
            padding: 20px;
            font-size: 30px;
            text-align: center;
        }
 
        /* Designing h1 element */
        h1 {
            color: green;
            text-align: center;
        }
    </style>
</head>
 
<body>
    <h1>GeeksforGeeks</h1>
 
    <!-- Creating grid -->
    <div class="grid-container">
        <div class="grid-item">1</div>
        <div class="grid-item">2</div>
        <div class="grid-item">3</div>
        <div class="grid-item">4</div>
        <div class="grid-item">5</div>
        <div class="grid-item">6</div>
        <div class="grid-item">7</div>
        <div class="grid-item">8</div>
        <div class="grid-item">9</div>
    </div>
</body>
 
</html>

Output:

Example 2: This example illustrates the use of display:inline-grid; property.

<!DOCTYPE html>
<html>
 
<head>
    <style>
        /* Designing all grid */
        .grid-container {
            display: inline-grid;
            grid-template-columns: auto auto auto;
            background-color: gray;
            padding: 5px;
        }
 
        /* Designing all grid-items */
        .grid-item {
            background-color: rgba(255, 255, 255, 0.8);
            border: 1px solid black;
            padding: 20px;
            font-size: 30px;
        }
 
        /* Designing h1 element */
        h1 {
            color: green;
            text-align: center;
        }
    </style>
</head>
 
<body>
    <center>
        <h1>GeeksforGeeks</h1>
 
        <!-- Creating grids -->
        <div class="grid-container">
            <div class="grid-item">1</div>
            <div class="grid-item">2</div>
            <div class="grid-item">3</div>
            <div class="grid-item">4</div>
            <div class="grid-item">5</div>
            <div class="grid-item">6</div>
            <div class="grid-item">7</div>
            <div class="grid-item">8</div>
            <div class="grid-item">9</div>
        </div>
    </center>
</body>
 
</html>

Output:

Screenshot-2023-07-13-125103

You can control the following things on a grid system:

    grid-column-gap
    grid-row-gap
    grid-gap

Example 3: In the below code we used both grid-column-gap and grid-row-gap together.

<!DOCTYPE html>
<html>
 
<head>
    <style>
        /* Designing all grid */
        .grid-container {
            display: grid;
            grid-template-columns: auto auto auto;
            background-color: gray;
            grid-column-gap: 50px;
            grid-row-gap: 50px;
            padding: 5px;
        }
 
        /* Designing all grid-items */
        .grid-item {
            background-color: rgba(255, 255, 255, 0.8);
            border: 1px solid black;
            padding: 20px;
            font-size: 30px;
            text-align: center;
        }
 
        /* Designing h1 element */
        h1 {
            color: green;
            text-align: center;
        }
    </style>
</head>
 
<body>
    <h1>GeeksforGeeks</h1>
 
    <!-- Creating grids -->
    <div class="grid-container">
        <div class="grid-item">1</div>
        <div class="grid-item">2</div>
        <div class="grid-item">3</div>
        <div class="grid-item">4</div>
        <div class="grid-item">5</div>
        <div class="grid-item">6</div>
        <div class="grid-item">7</div>
        <div class="grid-item">8</div>
        <div class="grid-item">9</div>
    </div>
</body>
 
</html>

Output:

Note: Similarly grid-gap also works.

You can control the following things on a grid system:

    grid-column-lines
    grid-row-lines

Example:4 In the below code we used both grid-column-lines and grid-row-lines together.

<!DOCTYPE html>
<html>
 
<head>
    <style>
        /* Designing all grid */
        .grid-container {
            display: grid;
            grid-template-columns: auto auto auto;
            grid-gap: 10px;
            background-color: gray;
            padding: 10px;
        }
 
        /* Designing all grid-items */
        .grid-container>div {
            background-color: rgba(255, 255, 255, 0.8);
            text-align: center;
            padding: 20px 0;
            font-size: 30px;
        }
 
        /* Grid Column */
        .item1 {
            grid-column-start: 1;
            grid-column-end: 3;
        }
 
        /* Grid row */
        .item3 {
            grid-row-start: 2;
            grid-row-end: 5;
        }
 
        /* Designing h1 element */
        h1 {
            color: green;
            text-align: center;
        }
    </style>
</head>
 
<body>
    <h1>GeeksforGeeks</h1>
 
    <!-- Creating grids -->
    <div class="grid-container">
        <div class="item1">1</div>
        <div class="item2">2</div>
        <div class="item3">3</div>
        <div class="item4">4</div>
        <div class="item5">5</div>
        <div class="item6">6</div>
        <div class="item7">7</div>
        <div class="item8">8</div>
    </div>
</body>
 
</html>
