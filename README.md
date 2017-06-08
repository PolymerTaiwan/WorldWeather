World Weather
=============
A simple sample app built with Polymer(1.0)

<img src="images/screenshot.png"></img>

Build
-----
This project requires [bower](https://bower.io/#install-bower) and [polymer-cli](https://www.polymer-project.org/2.0/docs/tools/polymer-cli)

First, install bower components
```
bower install
```

View the web page with polymer-cli server:
```
polymer serve --port 9487 --open
```
And finally, build optimized version of this web app(**TBD**)
```
polymer build
```

OpenWeatherMap API Key
----------------------
This sample use weather data from [OpenWeatherMap](https://openweathermap.org/). So please implement your own `api-key-storage` element inside `src/element/key-storage.html` file.

Sample imeplementation:
```
<script>
    Polymer({
        is: 'api-key-storage',

        properties: {
            openWeather: {
                type: String,
                value: 'YOUR_API_KEY',
                readOnly: true,
                notify: true
            }
        }
    });
</script>
```

For more information about how to get an API key, please refer the [official guide](https://openweathermap.org/appid).