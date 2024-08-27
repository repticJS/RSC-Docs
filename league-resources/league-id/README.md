# /league/:id

## Fetch League Information

<mark style="color:green;">`GET`</mark> `/league/:id`

This is used to grab all the information about that league.\
Such as Name, Season Number, Logo, etc.

**Response**

{% tabs %}
{% tab title="200" %}
```json
{
  "name": "",
  "seasonNumber": 0,
  "logo": "",
  "banner": ""
}
```
{% endtab %}

{% tab title="404" %}
```json
{
  "error": "League not found",
  "status": 404
}
```
{% endtab %}
{% endtabs %}
