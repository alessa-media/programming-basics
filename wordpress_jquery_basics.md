# jQuery-basics
* jQuery wird meistens im Zusammenhang mit WordPress gebraucht.
* jQuery ist eine Javascript-Library.

## Beginn von jedem jQuery
```js
$=jQuery
$(document).ready(function (){
```

## Variablen
```js
  var test = "testvalue";
```

## Hooks

|     Hook                               |     Möglichkeit                               | 
|----------------------------------------|-----------------------------------------------|
|     wp_ajax_<funktionsname>            |     Nur für angemeldete Benutzer verfügbar    |
|     wp_ajax_nopriv_<funtktionsname>    |     Für alle Benutzer verfügbar               |

## Ajax-Call
* ein Ajax-Call ist typischerweise auf drei Ebenen mit sich verbunden.
  * Im Backend, normalerweise PHP
  * Im Frontend, einmal HTML für die Darstellung und einmal Javascript für die Funktion

### Beispiel
__PHP - Backend__
```php
add_action("wp_ajax_testfunction", "testfunction"); //logged in users -> admin dashboard
add_action("wp_ajax_nopriv_testfunction", "testfunction"); //not logged in users -> frontend
function testfunction(){
    $productID = $_POST['productID'];
    echo json_encode(array(
        'productID' => $productID,
        'value' => get_field("min_age", $productID),
    ));   
    wp_die();
}
```
__HTML - Frontend__
```html
<button class="button">datum ansehen</button>
```
__Javascript - Frontend__
```js
$('.button').click(function (e) { 
        e.preventDefault(); //do not reload forms when clicked
        $.ajax({ 
            url: '/wp-admin/admin-ajax.php', //always the same
            type: 'POST', //also stay the same
            data: {
                action: 'testfunction', //funktion im backend -> gleicher name!!!
                productID: $(this).parent().attr("productid"),
            },
            success: function (response) {
                var responseJSON = JSON.parse(response)
                $('[productID=' + responseJSON.productID + ']').append(responseJSON.value);
            },
        });
    });
```





  
