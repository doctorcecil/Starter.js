//James Smyth 02/08/2013.

$(document).ready(function () {
    Run.Init();
});

var Run = (function () {

    return {

        //Selectors, Classes and Values referenced here.
        //These are referenced like this 'Run.Selectors.Body'.
        //'Body' is within the Array of 'Selectors' which sits within the 'Run' function.
        Selectors: {
            Body: 'body',
            Header: 'header',
            Aside: 'aside',
            Sector: 'sector',
            Article: 'article',
            Footer: 'footer',
  		ImageSection: 'section#images'
        },

        //Typical classes below. But I usually use classes relating to animation and states such as 'open', 'closed' and 'animating'.
        Classes: {
            Desktop: 'desktop',
            Tablet: 'tablet',
            Mobile: 'mobile'
        },

        //Values of screen sizes below are standard but can change/be changed. I also use time values such as milliseconds for animation here.
        Values: {
            Desktop: 1024,
            Tablet: 768,
            Mobile: 767
        },

        //Run.Init() is where the top level function calls are. You would run a function checking if a certain section on a page exists and if so,
        //initialise that sections function. (line 46 is an example of this).
        Init: function () {
		    
            //Calls the function that adds a class to the body of what the screen dimension is.
            DeviceType.Init();

            //When the window is resized, whatever within this function is called.
            $(window).resize(function () {
                Resize.Init();
            });
			
            //Checking if 'section#images' exists on the page. If it does, 'Media.Init() is called.
		    if ($(Run.Selectors.ImageSection).length) {
				Media.Init();
			};
        }
    }
})();

//This function is called from line 45.
var Resize = (function () {
    return {
        Init: function () {

            DeviceType.Init();
        }
    }
})();


//This function is called from line 42.
var DeviceType = (function () {
    return {
        Init: function () {

            //Getting screen width then checking against 3 'if' statements.
            //Depending what value the variable 'width' is, Either 'Desktop.Init()', 'Tablet.Init()' or 'Mobile.Init()' will be called.
            //All 3 functions above will remove dimension classes from the body and replace them with the current dimensions class.
            var width = $(window).width();

            if (width > Run.Values.Tablet) {
                Desktop.Init();
            };

            if ((width >= Run.Values.Tablet) && (width < Run.Values.Desktop)) {
                Tablet.Init();
            };

            if ((width <= Run.Values.Mobile)) {
                Mobile.Init();
            };
        }
    }
})();

//This function is called on line 80.
var Desktop = (function () {
    return {
        Init: function () {

            $(Run.Selectors.Body).removeClass('tablet mobile').addClass(Run.Classes.Desktop);
        }
    }
})();

//This function is called on line 84.
var Tablet = (function () {
    return {
        Init: function () {

            $(Run.Selectors.Body).removeClass('desktop mobile').addClass(Run.Classes.Tablet);
        }
    }
})();

//This function is called on line 88.
var Mobile = (function () {
    return {
        Init: function () {

            $(Run.Selectors.Body).removeClass('desktop tablet').addClass(Run.Classes.Mobile);
        }
    }
})();

//This function is called on line 50.
var Media = (function () {
    return {
        Init: function () {
            //When the body is clicked 'Media.Example()' will be called.
            $(Run.Selectors.Body).click(Media.Example);
        },
		
		Example: function () {
		    //Media.Example() has been called and an alert event has occurred.
            alert("The body has been clicked");
        }
    }
})();
