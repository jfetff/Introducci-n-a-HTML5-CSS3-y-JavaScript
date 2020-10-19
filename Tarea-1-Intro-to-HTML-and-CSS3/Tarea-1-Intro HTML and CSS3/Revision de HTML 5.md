# Revision de CSS3

DESCRIPCION

## CSS3

#### CSS3 Selectors
    <div>Exercise:
    Change the color of all &lt;p&gt; elements to "red".
    
        <!DOCTYPE html>
        <html>
        <head>
            <style>
                p{
                    color: red;
                }
            </style>
            </head>
            <body>

                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>

            </body>
            </html>
    </div>
        <div>
        <strong>Exercise:</strong>
        Change the color of the element with id="para1", to "red".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
            #para1{
                color: red;
            }
            </style>
            </head>
            <body>

                <h1>This is a Heading</h1>
                <p id="para1">This is a paragraph.</p>
                <p>This is another paragraph.</p>

            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Change the color of all elements with the class "colortext", to "red".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
            .colortext{
                color: red;
            }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p class="colortext">This is another paragraph.</p>
                <p class="colortext">This is also a paragraph.</p>
            
            </body>
            </html>
             
	</div>
    <div><strong>Exercise:</strong>
        Change the color of all &lt;p&gt; and &lt;h1&gt; elements, to "red". Group the selectors to minimize code.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1, p {
                color: red;
                }
            </style>
            </head>
            <body>

                <h1>This is a heading</h1>
                <h2>This is a smaller heading</h2>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>

            </body>
            </html>
	</div>

#### CSS3 How To...
    <div><strong>Exercise:</strong>
    Add an external style sheet with the URL: "mystyle.css".
        <!DOCTYPE html>
        <html>
            <head>
                <link rel="stylesheet" href="mystyle.css">
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Set "background-color: linen" for the page, using an internal style sheet.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                body{
                    background-color: linen;
                } 
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Set "background-color: linen" for the page, using an inline style.
            <!DOCTYPE html>
            <html>
            <head>
            </head>
            <body style="background-color:linen;">
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
            
    </div>
    <div><strong>Exercise:</strong>
        Remove all styles, except the external style sheet "mystyle.css".
            <!DOCTYPE html>
            <html>
            <head>
                <link rel="stylesheet" href="mystyle.css">
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>  
    </div>

#### CSS3 Backgrounds
    <div><strong>Exercise:</strong>
        Set the background color for the page to "linen" and the background color for &lt;h1&gt; to "lightblue".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                body{
                    background-color: linen;
                }
                h1{
                    background-color: lightblue;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Set "paper.gif" as the background image of the page.
        <!DOCTYPE html>
        <html>
        <head>
        <style>
            body{
                background-image: url(paper.gif);
            }
        </style>
        </head>
        <body>
        
            <h1>This is a Heading</h1>
            <p>This is a paragraph.</p>
            <p>This is another paragraph.</p>
        
        </body>
        </html>
    </div>
    <div><strong>Exercise:</strong>
        Set "gradient_bg_vertical.png" as the background image of the page, and repeat it vertically only.
        <!DOCTYPE html>
        <html>
        <head>
        <style>
            body{
            background-image: url("gradient_bg_vertical.png");
            background-repeat: repeat-y;
            }
        </style>
        </head>
        <body>
        
            <h1>This is a Heading</h1>
            <p>This is a paragraph.</p>
            <p>This is another paragraph.</p>
        
        </body>
        </html>
	</div>
    <div><strong>Exercise:</strong>
        Specify that the background image should be shown once, in the top right corner.
        <!DOCTYPE html>
        <html>
        <head>
        <style>
            body {
            background-image: url("img_tree.png");
            background-repeat: no-repeat;
            background-position: top right;
        }
        </style>
        </head>
        <body>
        
            <h1>This is a Heading</h1>
            <p>This is a paragraph.</p>
            <p>This is another paragraph.</p>
        
        </body>
        </html>
    </div>
    <div><strong>Exercise:</strong>
        Use the shorthand background property to set background image to "img_tree.png", show it once, in the top right corner.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                body {
                    background: url('img_tree.png') no-repeat top right;
                }
            </style>
            </head>
            <body>

                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>

            </body>
            </html>
	</div>

#### CSS3 Border
    <div><strong>Exercise:</strong>
        Set a "4px", "dotted" border for <p>.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p {
                border-style: dotted;
                border-width: 4px;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Set the border color for <p> to "red".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p {
                border-style: dotted;
                border-width: 4px;
                border-color: red;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Change the 3 border properties, so that they only show the border on the top side.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p {
                    border-top-style: dotted;
                    border-top-width: 4px;
                    border-top-color: red;
                }
            </style>
            </head>
            <body>        
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        With the border property: Set the border for p to "10px", "solid" and "green".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p {
                    border-style: solid;
                    border-color: green;
                    border-width: 10px;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
            
            </body>
            </html>
    </div>
#### CSS3 Margin
    <div><strong>Exercise:</strong>
        Set the left margin of <h1> to "20px".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                background-color: lightblue;
                margin-left: 20px;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Set all margins for <h1> to "25px".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                background-color: lightblue;
                margin: 25px;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Use the margin property to set the top and bottom margins for &lt;h1&gt; to "50px", and left and right margins to "25px".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                background-color: lightblue;
                margin: 50px 25px;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Use the margin property to center align the &lt;h1&gt; element.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                background-color: lightblue;
                width: 300px;
                margin: auto;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
            
            </body>
            </html>
            
	</div>
#### CSS3 Padding
    <div><strong>Exercise:</strong>
        Set the top padding of &lt;p&gt; to "30px".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p {
                background-color: lightblue;
                padding-top: 30px;
                }
            </style>
            </head>
            <body>

                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>

            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Set all paddings for <p> to "50px".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p {
                background-color: lightblue;
                padding: 50px;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
            
            </body>
            </html>         
	</div>
    <div><strong>Exercise:</strong>
            Use the padding property to set the top and bottom paddings for &lt;p&gt; to "25px", and left and right paddings to "50px".
                <!DOCTYPE html>
                <html>
                <head>
                <style>
                    p {
                    background-color: lightblue;
                    padding: 25px 50px;
                    }
                </style>
                </head>
                <body>
                
                    <h1>This is a Heading</h1>
                    <p>This is a paragraph.</p>
                
                </body>
                </html>
    </div>
#### CSS3 Height/Width
    <div><strong>Exercise:</strong>
        Set the height of &lt;h1&gt; to "100px".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                background-color: lightblue;
                height: 100px;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Set the width of <h1> to "50%".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                background-color: lightblue;
                width: 50%;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
            
            </body>
            </html>
	</div>
#### CSS3 Box Model
    <div><strong>Exercise:</strong>
        Set the width of the div to "200px".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div {
                background-color: lightblue;
                width: 200px;
                }
            </style>
            </head>
            <body>
            
                <div>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</div>
            
            </body>
            </html>        
	</div>
    <div><strong>Exercise:</strong>
        Set the padding of the div to "25px".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div {
                background-color: lightblue;
                width: 200px;
                padding: 25px;
                }
            </style>
            </head>
            <body>
            
                <div>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</div>
            
            </body>
            </html>          
	</div>
    <div><strong>Exercise:</strong>
        Set the border of the div to "25px solid navy".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div {
                background-color: lightblue;
                width: 200px;
                padding: 25px;
                border: 25px solid navy;
                }
            </style>
            </head>
            <body>
            
                <div>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</div>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Set the margin of the div to "25px".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div {
                background-color: lightblue;
                width: 200px;
                padding: 25px;
                border: 25px solid navy;
                margin: 25px;
                }
            </style>
            </head>
            <body>
            
                <div>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</div>
            
            </body>
            </html>
	</div>
#### CSS3 Outline</h1>
    <div><strong>Exercise:</strong>
        Set a "solid", "5px" outline for &lt;p&gt;.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p {
                outline-style: solid;
                outline-width: 5px;
                }
            </style>
            </head>
            <body>

                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>

            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Set the outline color for <p> to "green".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p {
                outline-style: solid;
                outline-width: 4px;
                outline-color: green;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        With the outline property: Set the outline for p to "red", "dotted" and "10px".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p{
                    outline-style: dotted;
                    outline-width: 10px;
                    outline-color: red;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
            
            </body>
            </html>
	</div>
#### CSS3 Text
    <div><strong>Exercise:</strong>
        Set the text color for the page to "red", and the text color for &lt;h1&gt; to "blue".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                body{
                    color:red;
                }
                h1{
                    color: blue;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Center align the <h1> element.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1{
                    text-align: center;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Remove the underline from the link.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                a{
                    text-decoration: none;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p><a href="css_text.asp">CSS text tutorial</a></p>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Style text in &lt;h1&gt; to uppercase letters, and text in &lt;p&gt; to capitalized letters.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                    text-transform: uppercase;
                }
                p {
                    text-transform: capitalize;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>              
	</div>
    <div><strong>Exercise:</strong>
        Indent the first line of the &lt;p&gt; element with 20px.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p {
                    text-indent: 20px;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum</p>
                
            </body>
            </html>
	</div>
#### CSS3 Font
    <div><strong>Exercise:</strong>
        Set the font family for the page to "Courier New", and the font family for &lt;h1&gt; to "Verdana".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                body{
                    font-family: Courier New;
                }
                h1{
                    font-family: Verdana;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Show <p> elements as "italic" text.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p{
                    font-style: italic;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>                
	</div>
    <div><strong>Exercise:</strong>
        Set the font size for the page to "20px", and the font size for &lt;h1&gt; to "3em".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                body{
                    font-size: 20px;
                }
                h1{
                    font-size: 3em;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Show <p> elements as "bold" text.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p {
                font-weight: bold;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        With the font property: Set the &lt;p&gt; to "italic", "20px" and "Verdana".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p{
                    font-style: italic;
                    font-size: 20px;
                    font-family: Verdana;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
	</div>
#### CSS3 Links
    <div><strong>Exercise:</strong>
        Set the color for links to "green".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                a{
                    color: green;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p><a href="https://www.w3schools.com">W3Schools.com</a></p>
            
            </body>
            </html>          
	</div>
    <div><strong>Exercise:</strong>
        Set the color for unvisited links to "red", and the color for visited links "blue".
        <!DOCTYPE html>
        <html>
        <head>
        <style>
            /* unvisited link */
            a:link {
                color: red;
            }
            
            /* visited link */
            a:visited {
                color: blue;
            }
            
            /* mouse over link */
            a:hover {
                color: black;
            }
            
            /* selected link */
            a:active {
                color: green;
            }
        </style>
        </head>
        <body>
        
            <h1>This is a Heading</h1>
            <p>This is a paragraph.</p>
            <p><a href="https://www.w3schools.com">W3Schools.com</a></p>
        
        </body>
        </html>
	</div>
    <div><strong>Exercise:</strong>
        Remove underlines for visited and unvisited links, and specify "underline" for the hover and active link states.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                /* unvisited link */
                a:link {
                text-decoration: none;
                }
                
                /* visited link */
                a:visited {
                text-decoration: none;
                }
                
                /* mouse over link */
                a:hover {
                text-decoration: underline;
                }
                
                /* selected link */
                a:active {
                text-decoration: underline;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p><a href="https://www.w3schools.com">W3Schools.com</a></p>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
            Set the background color for visited and unvisited links to "lightblue", and the background color for the hover and active link states to "yellow".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                /* unvisited link */
                a:link {
                    background-color: lightblue;
                }
    
                /* visited link */
                a:visited {
                    background-color: lightblue;
                }
    
                /* mouse over link */
                a:hover {
                    background-color: yellow;
                }
    
                /* selected link */
                a:active {
                    background-color: yellow;
                }
            </style>
            </head>
            <body>
    
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p><a href="https://www.w3schools.com">W3Schools.com</a></p>
    
            </body>
            </html>
    </div>

#### CSS3 Lists
    <div><strong>Exercise:</strong>
        Set the list style for unordered lists to "square", and the list style for ordered lists to "upper-roman".
        <!DOCTYPE html>
        <html>
        <head>
        <style>
            ul {
            list-style-type: square;
            }
            
            ol {
            list-style-type: upper-roman;
            }
        </style>
        </head>
        <body>
        
            <p>This is an unordered list:</p>
            <ul>
                <li>Coffee</li>
                <li>Tea</li>
                <li>Coca Cola</li>
            </ul>
            
            <p>This is an ordered list:</p>
            <ol>
                <li>Coffee</li>
                <li>Tea</li>
                <li>Coca Cola</li>
            </ol>
            
        </body>
        </html>
	</div>
    <div><strong>Exercise:</strong>
        Set the image "sqpurple.gif" as the list item marker for the unordered list.
        <!DOCTYPE html>
        <html>
        <head>
        <style>
            ul{
                list-style-image: url('sqpurple.gif');
            }
        </style>
        </head>
        <body>

        <p>This is an unordered list:</p>
        <ul>
            <li>Coffee</li>
            <li>Tea</li>
            <li>Coca Cola</li>
        </ul>

        </body>
        </html>
    </div>
    <div><strong>Exercise:</strong>
        With the list-style property: Set the unordered list marker to "img_marker.png", with a backup style of "circle", and display the markers inside the content flow.
        <!DOCTYPE html>
        <html>
        <head>
        <style>
            ul {
                list-style: circle inside url('img_marker.png');
            }
        </style>
        </head>
        <body>

        <p>This is an unordered list:</p>
        <ul>
            <li>Coffee</li>
            <li>Tea</li>
            <li>Coca Cola</li>
        </ul>

        </body>
        </html>
    </div>
    <div><strong>Exercise:</strong>
        Remove the bullets/markers from the list items.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                ul{
                    list-style-type: none;
                }
            </style>
            </head>
            <body>
            
            <ul>
                <li>Coffee</li>
                <li>Tea</li>
                <li>Coca Cola</li>
            </ul>
            
            </body>
            </html>
	</div>
#### CSS3 Tables</h1>
    <div><strong>Exercise:</strong>
        Set the border to "2px solid green" for table, th and td elements.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                table, th, td {
                border: 2px solid green;
                }
            </style>
            </head>
            <body>
            
            <table>
              <tr>
                <th>Firstname</th>
                <th>Lastname</th>
              </tr>
              <tr>
                <td>Peter</td>
                <td>Griffin</td>
              </tr>
              <tr>
                <td>Lois</td>
                <td>Griffin</td>
              </tr>
            </table>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Collapse the table borders into a single border.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                table {
                    border-collapse: collapse;
                }
                table, td, th {
                    border: 1px solid black;
                }
            </style>
            </head>
            <body>
            
            <table>
                <tr>
                    <th>Firstname</th>
                    <th>Lastname</th>
                </tr>
                <tr>
                    <td>Peter</td>
                    <td>Griffin</td>
                </tr>
                <tr>
                    <td>Lois</td>
                    <td>Griffin</td>
                </tr>
            </table>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Set the width of the table to "100%".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                table {
                    width: 100%;
                }
                table, td, th {
                    border: 1px solid black;
                }
            </style>
            </head>
            <body>
            
            <table>
                <tr>
                    <th>Firstname</th>
                    <th>Lastname</th>
                </tr>
                <tr>
                    <td>Peter</td>
                    <td>Griffin</td>
                </tr>
                <tr>
                    <td>Lois</td>
                    <td>Griffin</td>
                </tr>
            </table>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Set the text alignment in &lt;td&gt; elements to "right".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                table, td, th {
                    border: 1px solid black;
                }
                table, td{
                    text-align: right;
                }
            </style>
            </head>
            <body>
            
            <table>
              <tr>
                <th>Firstname</th>
                <th>Lastname</th>
              </tr>
              <tr>
                <td>Peter</td>
                <td>Griffin</td>
              </tr>
              <tr>
                <td>Lois</td>
                <td>Griffin</td>
              </tr>
            </table>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Set the padding in &lt;th&gt; elements to "15px".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                table, td, th {
                    border: 1px solid black;
                }
                th {
                    padding: 15px;
                }
            </style>
            </head>
            <body>
            
            <table>
              <tr>
                <th>Firstname</th>
                <th>Lastname</th>
              </tr>
              <tr>
                <td>Peter</td>
                <td>Griffin</td>
              </tr>
              <tr>
                <td>Lois</td>
                <td>Griffin</td>
              </tr>
            </table>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Set the background color of &lt;th&gt; elements to "lightblue".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
            table, td, th {
              border: 1px solid black;
            }
            th {
              background-color: lightblue;
            }
            </style>
            </head>
            <body>
            
            <table>
              <tr>
                <th>Firstname</th>
                <th>Lastname</th>
              </tr>
              <tr>
                <td>Peter</td>
                <td>Griffin</td>
              </tr>
              <tr>
                <td>Lois</td>
                <td>Griffin</td>
              </tr>
            </table>
            
            </body>
            </html>
	</div>

#### CSS3 Display/Visibility
    <div><strong>Exercise:</strong>
        Hide the &lt;h1&gt; element. It should still take up the same space as before.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                visibility: hidden;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>        
	</div>
    <div><strong>Exercise:</strong>
        Hide the <h1> element. It should not take up any space.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                display: none;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Display the list items as inline elements
        <!DOCTYPE html>
        <html>
        <head>
        <style>
            ul, li {
                display: inline;
            }
        </style>
        </head>
        <body>
        
        <h1>This is a Heading</h1>
        
        <ul>
          <li>Apple</li>
          <li>Orange</li>
          <li>Pear</li>
        </ul>
        
        </body>
        </html>
    </div>
    <div></div><strong>Exercise:</strong>
        Display the &lt;strong&gt; elements as block elements.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                strong{
                    display: block;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a <strong>paragraph</strong>, with some words more <strong>important</strong> than others </p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>              
	</div>

#### CSS3 Positioning
    <div><strong>Exercise:</strong>
        Position the &lt;h1&gt; element to always be 50px from the top, and 50px from the right, relative to the window/frame edges.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                position: fixed;
                top: 50px;
                right: 50px;
                color: red;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>        
	</div>
    <div><strong>Exercise:</strong>
        Position the &lt;h1&gt; element 20px left, and 30px down, relative to its normal position.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                position: relative;
                top: 30px;
                left: -20px;
                color: red;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Position the &lt;h1&gt; element 50px from the left, and 100px from the top, relative to the HTML page.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                    position: absolute;
                    left: 50px;
                    top: 100px;
                color: red;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Position the &lt;img&gt; element behind the text.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                img {
                position: absolute;
                left: 0px;
                top: 0px;
                z-index: -1;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
                <img src="w3css.gif" width="100" height="140">
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Position the element with the "topleft" class 30px from the left, and 15px from the top, relative to its container.
        <!DOCTYPE html>
        <html>
        <head>
        <style>
            .container {
                position: relative;
            }
            
            .topleft {
                font-size: 18px;
                position: absolute;
                left: 30px;
                top: 15px;
            }
            
            img {
                width: 100%;
                height: auto;
                opacity: 0.3;
            }
        </style>
        </head>
        <body>
        
        <div class="container">
          <img src="img_5terre.jpg" alt="Cinque Terre" width="1000" height="300">
          <div class="topleft">Top Left</div>
        </div>
        
        </body>
        </html>
	</div>

#### CSS3 Overflow
    <div><strong>Exercise:</strong>
        Add a scrollbar to the &lt;div&gt; element.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div {
                background-color: #eee;
                width: 200px;
                height: 70px;
                border: 1px dotted black;
                overflow: scroll;
                }
            </style>
            </head>
            <body>
            
            <div>
              <p>In my younger and more vulnerable years my father gave me some advice that I've been turning over in my mind ever since.</p>
              <p>'Whenever you feel like criticizing anyone,' he told me, 'just remember that all the people in this world haven't had the advantages that you've had.'</p>
            </div>
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Specify that the overflowing text in the &lt;div&gt; element should not be visible, not even with scrolling.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div {
                  background-color: lightblue;
                  width: 200px;
                  height: 200px;
                  overflow: hidden;
                }
                </style>
                </head>
                <body>
                
                    <div>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</div>
                
                </body>
                </html>
	</div>
    <div><strong>Exercise:</strong>
        Add a horizontal scrollbar to &lt;div&gt;.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div {
                background-color: #eee;
                width: 150px;
                height: 70px;
                border: 1px dotted black;
                white-space: nowrap;
                overflow-x: scroll;
                }
            </style>
            </head>
            <body>
            
            <div>
              <p>In my younger and more vulnerable years my father gave me some advice that I've been turning over in my mind ever since.</p>
            </div>
            
            </body>
            </html>
	</div>

#### CSS3 Align
    <div><strong>Exercise:</strong>
        Center align the &lt;div&gt; element using margins.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div {
                    width: 300px;
                    background-color: #b0e0e6;
                    margin: auto;
                }
            </style>
            </head>
            <body>
            
            <div>
              <p>In my younger and more vulnerable years my father gave me some advice that I've been turning over in my mind ever since.</p>
              <p>'Whenever you feel like criticizing anyone,' he told me, 'just remember that all the people in this world haven't had the advantages that you've had.'</p>
            </div>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Position the &lt;div&gt; element all the way to the right using absolute positioning.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div {
                    width: 300px;
                    background-color: #b0e0e6;
                    position: absolute;
                    right: 0px;
                }
            </style>
            </head>
            <body>
            
            <div>
              <p>In my younger and more vulnerable years my father gave me some advice that I've been turning over in my mind ever since.</p>
              <p>'Whenever you feel like criticizing anyone,' he told me, 'just remember that all the people in this world haven't had the advantages that you've had.'</p>
            </div>
            
            </body>
            </html>
	</div>

#### CSS3 Combinators
    <div><strong>Exercise:</strong>
        Change the color of all &lt;p&gt; elements, that are descendants of &lt;div&gt; elements, to "red".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div, p{
                    color: red;
                }
            </style>
            </head>
            <body>
            
            <div>
              <p>This is a paragraph inside a div element.</p>
              <p>This is another paragraph inside a div element.</p>
              <span><p>This a paragraph inside a span element, inside a div element.</p></span>
            </div>
            
                <p>This is a paragraph, not inside a div element.</p>
                <p>This is another paragraph, not inside a div element.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Change the color of all &lt;p&gt; elements, that are immediate children of &lt;div&gt; elements, to "red".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div > p {
                    color: red;
                }
            </style>
            </head>
            <body>
            
            <div>
              <p>This is a paragraph inside a div element.</p>
              <p>This is another paragraph inside a div element.</p>
              <span><p>This a paragraph inside a span element, inside a div element.</p></span>
            </div>
            
            <p>This is a paragraph, not inside a div element.</p>
            <p>This is another paragraph, not inside a div element.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Change the color of &lt;p&gt; elements, that are the adjacent (immediately following) sibling of a &lt;div&gt; element, to "red".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div + p {
                    color: red;
                }
            </style>
            </head>
            <body>
            
            <div>
              <p>This is a paragraph inside a div element.</p>
              <p>This is another paragraph inside a div element.</p>
              <span><p>This a paragraph inside a span element, inside a div element.</p></span>
            </div>
            
            <p>This is a paragraph, not inside a div element.</p>
            <p>This is another paragraph, not inside a div element.</p>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Change the color of &lt;p&gt; elements, that are the siblings of a &lt;div&gt; element, to "red".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div ~ p {
                    color: red;
                }
            </style>
            </head>
            <body>
            
            <div>
              <p>This is a paragraph inside a div element.</p>
              <p>This is another paragraph inside a div element.</p>
              <span><p>This a paragraph inside a span element, inside a div element.</p></span>
            </div>
            
            <p>This is a paragraph, not inside a div element.</p>
            <p>This is another paragraph, not inside a div element.</p>
            
            </body>
            </html>
	</div>

#### CSS3 Pseudo-class
    <div><strong>Exercise:</strong>
        Set the background color for visited and unvisited links to "lightblue", and the background color for the hover and active link states to "yellow".
        <!DOCTYPE html>
        <html>
        <head>
        <style>
            /* unvisited link */
            a:link {
                background-color: lightblue;
            }
            
            /* visited link */
            a:visited {
                background-color: lightblue;
            }
            
            /* mouse over link */
            a:hover {
                background-color: yellow;
            }
            
            /* selected link */
            a:active {
                background-color: yellow;
            }
        </style>
        </head>
        <body>
        
            <h1>This is a Heading</h1>
            <p>This is a paragraph.</p>
            <p><a href="https://www.w3schools.com">W3Schools.com</a></p>
        
        </body>
        </html>
	</div>
    <div><strong>Exercise:</strong>
        Change the background color, when a user hovers over p elements, with the class "highlight", to "lightblue".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                /* mouse over p */
                p.highlight:hover {
                    background-color: lightblue;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p class="highlight">This is another paragraph.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Set the background color of &lt;p&gt; elements, that are the first child of any element, to "lightblue".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p:first-child {
                    background-color: lightblue;
                }
            </style>
            </head>
            <body>
            
                <p>This is a paragraph.</p>
                <p>This is also a paragraph</p>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Set the background color of &lt;input&gt; elements that are in focus (clicked or active), to "lightblue".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                input:focus {
                    background-color: lightblue;
                }
            </style>
            </head>
            <body>
            
            <form action="/action_page.php" method="get">
                First name: <input type="text" name="fname"><br>
                Last name: <input type="text" name="lname"><br>
                <input type="submit" value="Submit">
            </form>
            
            </body>
            </html>
	</div>

#### CSS3 Pseudo-elements
    <div><strong>Exercise:</strong>
        Set text color to red, for the first line of the &lt;p&gt; element.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p::first-line {
                    color: red;
                }
            </style>
            </head>
            <body>
            
                <p>In my younger and more vulnerable years my father gave me some advice that I've been turning over in my mind ever since. 'Whenever you feel like criticizing anyone,' he told me, 'just remember that all the people in this world haven't had the advantages that you've had.'</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Set text color to "red", and the text size to "xx-large", for the first letter of the &lt;p&gt; element.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p::first-letter {
                    color: red;
                    font-size: xx-large;
                }
            </style>
            </head>
            <body>
            
                <p>In my younger and more vulnerable years my father gave me some advice that I've been turning over in my mind ever since. 'Whenever you feel like criticizing anyone,' he told me, 'just remember that all the people in this world haven't had the advantages that you've had.'</p>
            
            </body>
            </html>              
	</div>
    <div><strong>Exercise:</strong>
        Insert the image "smiley.gif" before, and after &lt;p&gt; elements, using the ::before and ::after pseudo-elements.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p::before{
                    content: url(smiley.gif);
                }
                p::after{
                    content: url(smiley.gif);
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
	</div>

#### CSS3 Opacity
    <div><strong>Exercise:</strong>
        Set the transparency/opacity of the &lt;img&gt; element to "0.4".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                img {
                    opacity: 0.4;
                }
            </style>
            </head>
            <body>
            
                <img src="klematis.jpg" width="150" height="113">
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Remove the transparency/opacity of the &lt;img&gt; element when the user hovers over it with the mouse pointer.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                img {
                    opacity: 0.4;
                }
                img:hover {
                    opacity: 1.0;
                }
            </style>
            </head>
            <body>
            
                <img src="klematis.jpg" width="150" height="113">
            
            </body>
            </html>
	</div>

#### CSS3 Attribute Selectors
    <div><strong>Exercise:</strong>
        Set the background-color to "lightblue" for elements with a "target" attribute.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                a[target]{
                    background-color: lightblue;
                }
            </style>
            </head>
            <body>
            
                <a href="https://www.w3schools.com">w3schools.com</a>
                <a href="http://www.disney.com" target="_blank">disney.com</a>
                <a href="http://www.wikipedia.org" target="_top">wikipedia.org</a>
            
            </body>
            </html>  
	</div>
    <div><strong>Exercise:</strong>
        Set the background-color to "lightblue" for elements with an attribute like: target="_blank"
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                a[target="_blank"] {
                    background-color: lightblue;
                }
            </style>
            </head>
            <body>
            
                <a href="https://www.w3schools.com">w3schools.com</a>
                <a href="http://www.disney.com" target="_blank">disney.com</a>
                <a href="http://www.wikipedia.org" target="_top">wikipedia.org</a>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Set a border with the color "red", around elements with a "title" attribute containing the word "red".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                [title~="red"] {
                    border: 5px solid red;
                }
            </style>
            </head>
            <body>
            
                <img src="klematis_small.jpg" title="two red flowers" width="107" height="90">
                <img src="klematis2_small.jpg" title="purple flower" width="107" height="80">
                <img src="klematis3_small.jpg" title="red flower" width="116" height="90">
                <img src="klematis4_small.jpg" title="two white flowers" width="120" height="90">
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Set a border with the color "red", around elements with a "title" attribute starting with "red".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                [title^="red"] {
                border: 5px solid red;
                }
            </style>
            </head>
            <body>
            
                <img src="klematis_small.jpg" title="two red flowers" width="107" height="90">
                <img src="klematis2_small.jpg" title="purple flower" width="107" height="80">
                <img src="klematis3_small.jpg" title="red flower" width="116" height="90">
                <img src="klematis4_small.jpg" title="two white flowers" width="120" height="90">
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Set a border with the color "red", around elements with a "title" attribute ending with the word "flower" (not flowers).
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                [title$="flower"] {
                    border: 5px solid red;
                }
            </style>
            </head>
            <body>
            
                <img src="klematis_small.jpg" title="two red flowers" width="107" height="90">
                <img src="klematis2_small.jpg" title="purple flower" width="107" height="80">
                <img src="klematis3_small.jpg" title="red flower" width="116" height="90">
                <img src="klematis4_small.jpg" title="two white flowers" width="120" height="90">
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Set a border with the color "red", around elements with a "title" attribute containing the value "flow".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                [title*="flow"] {
                border: 5px solid red;
                }
            </style>
            </head>
            <body>
            
                <img src="klematis_small.jpg" title="two red flowers" width="107" height="90">
                <img src="klematis2_small.jpg" title="purple flower" width="107" height="80">
                <img src="klematis3_small.jpg" title="red flower" width="116" height="90">
                <img src="klematis4_small.jpg" title="two white flowers" width="120" height="90">
            
            </body>
            </html>
	</div>

#### CSS3 Rounded Corners
    <div><strong>Exercise:</strong>
        Give the &lt;div&gt; element rounded corners (use the shorthand property and the value "25px").
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    background: #73AD21;
                    padding: 20px; 
                    width: 200px;
                    border-radius: 25px;
                }
            </style>
            </head>
            <body>
            
                <div>This is a div element. It has some text.</div>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Give the &lt;div&gt; element a rounded corner (25px radius) on the bottom left side.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    border-bottom-left-radius: 25px;
                    background: #73AD21;
                    padding: 20px; 
                    width: 200px;  
                }
            </style>
            </head>
            <body>
            
                <div>This is a div element. It has some text.</div>
            
            </body>
            </html>
	</div>

#### CSS3 Border Images
    <div><strong>Exercise:</strong>
        Give the &lt;div&gt; element an image border using the image "border.png". Slice the image at 30px and repeat it.

            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div { 
                    border: 10px solid;
                    border-image: url(border.png) 30 round;
                }
            </style>
            </head>
            <body>
            
                <div>This is a div element. It has some text.</div>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Give the &lt;div&gt; element an image border using the image "border.png". Slice the image at 30px and stretch it.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div { 
                    border: 10px solid;
                    border-image: url('border.png') 30 stretch;
                }
            </style>
            </head>
            <body>
            
                <div>This is a div element. It has some text.</div>
            
            </body>
            </html>
	</div>

#### CSS3 Backgrounds
    <div><strong>Exercise:</strong>
        Add a second background image ("img_flwr.gif") to the &lt;body&gt; element. Make sure that "img_flwr.gif" is displayed on top of the current background image.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                body {
                    background-image: url(img_flwr.gif), url(paper.gif);
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Change the size of the background image to: width 100px, height 80px.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                body {
                    background: url(img_flwr.gif);
                    background-repeat: no-repeat;
                    background-size: 100px 80px;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
        
	</div>
    <div><strong>Exercise:</strong>
        Change the size of the background image so it always fits the entire page.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                html { 
                    background: url(img_flower.jpg) no-repeat center center fixed;
                    background-size: cover;
                }
                
                body { 
                color: white; 
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Specify that the background image position should start from the upper left corner of the content-box.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div { 
                    border: 10px solid black;
                    padding: 35px;
                    background: url(img_flwr.gif);
                    background-repeat: no-repeat;
                    background-origin: content-box;
                }
            </style>
            </head>
            <body>
            
            <div>
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            </div>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Specify that the "painting area" of the background should be to the outside edge of the padding.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div { 
                    border: 10px dotted black;
                    padding: 35px;
                    background: lightblue;
                    background-clip: padding-box;
                }
            </style>
            </head>
            <body>
            
            <div>
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            </div>
            
            </body>
            </html>
	</div>

#### CSS3 Colors
       <div><strong>Exercise:</strong>
        Set the opacity for the background color of the &lt;h1&gt; element to "0.3" by using a RGBA color instead of RGB.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                    background-color: rgb(0,255,0, 0.3);
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Set the following HSL color as the background of the &lt;h1&gt; element: Set the Hue to red (0), Saturation to 100%, and lightness to 50%.

            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                    background-color: hsl(0,100%,50%);
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>	   
	</div>
    <div><strong>Exercise:</strong>
        Set the opacity for the background color of the &lt;h1&gt; element to "0.3" by using a HSLA color instead of HSL.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                    background-color: hsla(0,100%,50%,0.3);
                }
            </style>
            </head>
            <body>
                
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
                
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Set the transparency/opacity of the &lt;h1&gt; element to "0.4".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                    background-color: red;
                    opacity: 0.4;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
	</div>

#### CSS3 Gradients
    <div><strong>Exercise:</strong>
        Set a linear gradient background for the &lt;div&gt; element, going from the top to bottom, transitioning from "white" to "green".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div {
                    background-image: linear-gradient(white, green);
                }
            </style>
            </head>
            <body>
            
                <div style="height:200px"></div>
            
            </body>
            </html>
		
	</div>
    <div><strong>Exercise:</strong>
        Set a linear gradient background for the &lt;div&gt; element, going from the top left to the bottom right, transitioning from "white" to "green".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div {
                    background-image: linear-gradient(to bottom right, white, green);
                }
            </style>
            </head>
            <body>
            
                <div style="height:200px"></div>
            
            </body>
            </html>
		
	</div>
    <div><strong>Exercise:</strong>
        Set a linear gradient background for the &lt;div&gt; element, going at a 70 degree angle, transitioning from "white" to "green".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div {
                    background-image: linear-gradient(70deg, white, green);
                }
            </style>
            </head>
            <body>
            
                <div style="height:200px"></div>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Set a linear gradient background for the &lt;div&gt; element, going from the top to bottom, transitioning from "white" to "red" to "blue" to "green".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div {
                    background-image: linear-gradient(white, red, blue, green);
                }
            </style>
            </head>
            <body>
                
                <div style="height:200px"></div>
            
            </body>
            </html>
	   
    </div>
    <div><strong>Exercise:</strong>
        Set a linear gradient background for the &lt;div&gt; element, going from the top to bottom, transitioning from "rgba(0,255,0,0.2)" to "rgba(0,255,0,1)".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div {
                    background-image: linear-gradient(rgba(0,255,0,0.2), rgba(0,255,0,1));
                }
            </style>
            </head>
            <body>
            
                <div style="height:200px"></div>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Set a radial gradient background for the &lt;div&gt; element, transitioning from "white" to "green".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div {
                    background-image: radial-gradient(white, green);
                }
            </style>
            </head>
            <body>
            
                <div style="height:200px"></div>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Set a radial gradient background for the &lt;div&gt; element, with a circle shape, transitioning from "white" to "green".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div {
                    background-image: radial-gradient(circle, white, green);
                }
            </style>
            </head>
            <body>
            
                <div style="height:200px"></div>
            
            </body>
            </html>
	</div>

#### CSS3 Shadows Effects
    <div><strong>Exercise:</strong>
        Set a "2px" horizontal, and "2px" vertical, text shadow for the &lt;h1&gt; element.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                    text-shadow: 2px 2px;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Change the color of the text shadow to "green", and set a "5px" blur radius.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                    text-shadow: 2px 2px 5px green;
                }
            </style>
            </head>
            <body>
                       
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Add a new shadow (do not remove the current one) to the &lt;h1&gt; element with: no horizontal or vertical shadow, 10px blur, and a red color.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                h1 {
                    text-shadow: 2px 2px 5px green, 0px 0px 10px red;
                }
            </style>
            </head>
            <body>            
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Set a "10px" horizontal, and "10px" vertical, box shadow for the &lt;div&gt; element.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div {
                    box-shadow: 10px 10px;
                }
            </style>
            </head>
            <body>
            
            <div style="background-color: lightblue; width: 350px; padding: 15px;">
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            </div>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Change the color of the box shadow to "grey", and set a "5px" blur.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                div {
                    box-shadow: 10px 10px 5px grey;
                }
            </style>
            </head>
            <body>
            
            <div style="background-color: lightblue; width: 350px; padding: 15px;">
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            </div>
            
            </body>
            </html>
	</div>
#### CSS3 Text Effects
    <div><strong>Exercise:</strong>
        Specify that the overflowed content for the &lt;p&gt; element should be signaled with an ellipsis (...)
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p {
                    white-space: nowrap; 
                    width: 200px; 
                    border: 1px solid #000000;
                    overflow: hidden;
                    text-overflow: ellipsis;
                }
            </style>
            </head>
            <body>
            
                <p>This paragraph contains a very long word: supercalifragilisticexpialidocious.</p>
            
            </body>
            </html>
		
	</div>
    <div><strong>Exercise:</strong>
        Specify that text in the &lt;p&gt; element should wrap, even if it needs to split in the middle of a word.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p {
                    width: 150px; 
                    border: 1px solid #000000;
                    word-wrap: break-word;
                }
            </style>
            </head>
            <body>
            
                <p>This paragraph contains a very long word: supercalifragilisticexpialidocious.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Specify that text in the &lt;p&gt; element can break between any two letters.
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                p {
                    width: 150px; 
                    border: 1px solid #000000;
                    word-break: break-all;
                }
            </style>
            </head>
            <body>
            
                <p>This paragraph contains a very long word: super-cali-fragi-listic-expialidocious.</p>
            
            </body>
            </html>
	</div>

#### CSS3 Web Fonts
    <div><strong>Exercise:</strong>
        Add a web font with the name "sansation" and the URL "sansation_light.woff".
            <!DOCTYPE html>
            <html>
            <head>
            <style>
                @font-face {
                    font-family: sansation;
                    src: url(sansation_light.woff);
                }
                body {
                    font-family: sansation;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Add another @font-face rule for bold characters of the "sansation" font. Use the URL "sansation_bold.woff".
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                @font-face {
                    font-family: sansation;
                    src: url(sansation_light.woff);
                }
                
                @font-face {
                    font-family: sansation;
                    src: url(sansation_bold.woff);
                    font-weight: bold;
                }
                body {
                    font-family: sansation;
                }
            </style>
            </head>
            <body>
            
                <h1>This is a Heading</h1>
                <p>This is a paragraph.</p>
                <p>This is another paragraph.</p>
            
            </body>
            </html>
	</div>

#### CSS3 2D Transforms
    <div><strong>Exercise:</strong>
        With the transform property, move the &lt;div&gt; element 100px to the right, and 200px down.

            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    width: 100px;
                    height: 100px;
                    background-color: lightblue;
                    border: 1px solid black;
                    transform: translate(100px, 200px);
                }
            </style>
            </head>
            <body>
            
            <div></div>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        With the transform property, rotate the &lt;div&gt; element 45 degrees.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    width: 100px;
                    height: 100px;
                    margin: 50px;
                    background-color: lightblue;
                    border: 1px solid black;
                    transform: rotate(45deg);
                }
            </style>
            </head>
            <body>
            
            <div></div>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        With the transform property, change the size of the &lt;div&gt; to half its width, but double its height.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    width: 100px;
                    height: 100px;
                    margin: 50px;
                    background-color: lightblue;
                    border: 1px solid black;
                    transform: scale(0.5,2);
                }
            </style>
            </head>
            <body>
            
            <div></div>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        With the transform property, skew the &lt;div&gt; element 20 degrees along the X-axis, and 30 degrees along the Y-axis.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    width: 100px;
                    height: 100px;
                    margin: 50px;
                    background-color: lightblue;
                    border: 1px solid black;
                    transform: skew(20deg, 30deg);
                }
            </style>
            </head>
            <body>
            
                <div></div>
            
            </body>
            </html>
	</div>

#### CSS3 3D Transforms
    <div><strong>Exercise:</strong>
        With the transform property, rotate the &lt;div&gt; element 150deg around its X-axis.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    width: 100px;
                    height: 100px;
                    background-color: lightblue;
                    border: 1px solid black;
                    transform: rotateX(150deg);
                }
            </style>
            </head>
            <body>
            
                <div>This is a div element</div>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        With the transform property, rotate the &lt;div&gt; element 120deg around its Y-axis.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    width: 100px;
                    height: 100px;
                    background-color: lightblue;
                    border: 1px solid black;
                    transform: rotateY(120deg);
                }
            </style>
            </head>
            <body>
            
                <div>This is a div element</div>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        With the transform property, rotate the &lt;div&gt; element 90deg around its Z-axis.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    width: 100px;
                    height: 100px;
                    background-color: lightblue;
                    border: 1px solid black;
                    transform: rotateZ(90deg);
                }
            </style>
            </head>
            <body>
            
            <div>This is a div element</div>
            
            </body>
            </html>
	</div>

#### CSS3 Transitions
    <div><strong>Exercise:</strong>
        Add a 2 second transition effect for width changes of the &lt;div&gt; element.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    width: 100px;
                    height: 100px;
                    background: red;
                    transition: width 2s;
                }
                
                div:hover {
                    width: 300px;
                }
            </style>
            </head>
            <body>
            
            <div></div>
            
                <p>Hover over the div element above.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Specify that the transition of the &lt;div&gt; element should have a "ease-in-out" speed curve.

            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    width: 100px;
                    height: 100px;
                    background: red;
                    transition: width 2s ease-in-out;
                }
                
                div:hover {
                    width: 300px;
                }
            </style>
            </head>
            <body>
            
            <div></div>
            
            <p>Hover over the div element above.</p>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Specify that the transition of the &lt;div&gt; element should have a "0.5" second delay before starting.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    width: 100px;
                    height: 100px;
                    background: red;
                    transition: width 2s;
                    transition-delay: 0.5s;
                }
                
                div:hover {
                    width: 300px;
                }
            </style>
            </head>
            <body>
            
            <div></div>
            
                <p>Hover over the div element above.</p>
            
            </body>
            </html>

    </div>
    <div><strong>Exercise:</strong>
        Add a 2 second transition effect for background, and transform changes of the &lt;div&gt; element.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    width: 100px;
                    height: 100px;
                    background: red;
                    transition: background 2s, transform 2s;
                }
                
                div:hover {
                    background: blue;
                    transform: rotate(180deg);
                }
            </style>
            </head>
            <body>
            
            <div></div>
            
                <p>Hover over the div element above.</p>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Using the transition shorthand property, specify width changes for the &lt;div&gt; element should have:
        "2" second duration, "ease-in-out" speed curve, and a "0.5" second delay before starting.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    width: 100px;
                    height: 100px;
                    background: red;
                    transition: width 2s ease-in-out 0.5s;
                }
                
                div:hover {
                    width: 400px;
                }
            </style>
            </head>
            <body>
            
                <div></div>
            
                <p>Hover over the div element above.</p>
            
            </body>
            </html>
	</div>
    
#### CSS3 Animations
    <div><strong>Exercise:</strong>
        Add a 2 second animation for the &lt;div&gt; element, which changes the color from red to blue. Call the animation "example"
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    width: 100px;
                    height: 100px;
                    background-color: red;
                    animation-name: example;
                    animation-duration: 2s;
                }
                
                @keyframes example {
                    from {background-color: red;}
                    to {background-color: blue;}
                }
            </style>
            </head>
            <body>
            
            <div></div>
            
            </body>
            </html>

	</div>
    <div><strong>Exercise:</strong>
        Add the following 5 steps to the animation "example" (using 0%, 25%, 50%, 75%, and 100%):

        0% - Set background color to "red", left position to "0px", top position to: "0px"
        25% - Set background color to "blue", left position to "0px", top position to: "200px"
        50% - Set background color to "green", left position to "200px", top position to: "200px"
        75% - Set background color to "yellow", left position to "200px", top position to: "0px"
        100% - Set background color to "red", left position to "0px", top position to: "0px"

            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    width: 100px;
                    height: 100px;
                    position: relative;
                    background-color: red;
                    animation-name: example;
                    animation-duration: 4s;
                }

                @keyframes example {
                    0%   {background-color: red; left:0px; top:0px;}
                    25%  {background-color: blue; left:0px; top:200px;}
                    50%  {background-color: green; left:200px; top:200px;}
                    75%  {background-color: yellow; left:200px; top:0px;}
                    100% {background-color: red; left:0px; top:0px;}
                }
            </style>
            </head>
            <body>

                <div></div>

            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Specify that the animation of the &lt;div&gt; element should have a "1" second delay before starting.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    width: 100px;
                    height: 100px;
                    position: relative;
                    background-color: red;
                    animation-name: example;
                    animation-duration: 2s;
                    animation-delay: 1s;
                }
                
                @keyframes example {
                    0%   {background-color: red; left:0px;}
                    50%  {background-color: yellow; left:200px;}
                    100% {background-color: red; left:0px;}
                }
            </style>
            </head>
            <body>
            
                <div></div>
            
            </body>
            </html>
    </div>
    <div><strong>Exercise:</strong>
        Specify that the animation of the &lt;div&gt; element should continue to loop for ever.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    width: 100px;
                    height: 100px;
                    position: relative;
                    background-color: red;
                    animation-name: example;
                    animation-duration: 2s;
                    animation-iteration-count: infinite;
                }
                
                @keyframes example {
                    0%   {background-color: red; left:0px;}
                    50%  {background-color: yellow; left:200px;}
                    100% {background-color: red; left:0px;}
                }
            </style>
            </head>
            <body>
            
                <div></div>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Specify that the animation of the &lt;div&gt; element should alternate between running forwards and backwards.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    width: 100px;
                    height: 100px;
                    position: relative;
                    background-color: red;
                    animation-name: example;
                    animation-duration: 4s;
                    animation-iteration-count: infinite; 
                        animation-direction: alternate; 
                }
                
                @keyframes example {
                    0%   {background-color: red; left:0px; top:0px;}
                    25%  {background-color: blue; left:0px; top:200px;}
                    50%  {background-color: green; left:200px; top:200px;}
                    75%  {background-color: yellow; left:200px; top:0px;}
                    100% {background-color: red; left:0px; top:0px;}
                }
            </style>
            </head>
            <body>
            
                <div></div>
            
            </body>
            </html>
	</div>
    <div><strong>Exercise:</strong>
        Specify that the animation of the &lt;div&gt; element should have a "ease-in-out" speed curve.
            <!DOCTYPE html>
            <html>
            <head>
            <style> 
                div {
                    width: 100px;
                    height: 100px;
                    position: relative;
                    background-color: red;
                    animation-name: example;
                    animation-duration: 4s;
                    animation-timing-function: ease-in-out;
                }
                
                @keyframes example {
                    0%   {background-color: red; left:0px;}
                    50%  {background-color: yellow; left:200px;}
                    100% {background-color: red; left:0px;}
                }
            </style>
            </head>
            <body>
            
                <div></div>
            
            </body>
            </html>
	</div>      