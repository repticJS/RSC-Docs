---
description: All Authorized "User" routes.
---

# /user

<mark style="color:green;">`GET`</mark> `/user`

This is used a authorized method of fetching the user.\
If user does not exist it will create it, and send back the created data.

**Headers**

| Name          | Value              |
| ------------- | ------------------ |
| Content-Type  | `application/json` |
| Authorization | `Bearer <token>`   |

**Response**

{% tabs %}
{% tab title="200" %}
<pre class="language-json"><code class="lang-json"><strong>{
</strong>"discordId":""
"discordAccessToken":""
}
</code></pre>
{% endtab %}

{% tab title="401" %}
```json
{
"errorCode": 401,
"message": "unauthorized"
}
```
{% endtab %}
{% endtabs %}



<mark style="color:green;">`PUT`</mark> `/user/update`

This is used for updating the user.\
You pass what ever fields u want updating in the body.

**Headers**

| Name          | Value              |
| ------------- | ------------------ |
| Content-Type  | `application/json` |
| Authorization | `Bearer <token>`   |

**Body**

| Name     | Type   | Description          |
| -------- | ------ | -------------------- |
| username | string | Username of the user |
| socials  | object | Social Accounts      |

#### Socials object example

<pre><code><strong>{
</strong>    twitter: "",
    twitch: "",
    instagram: "",
    tiktok: ""
}
</code></pre>

**Response**

{% tabs %}
{% tab title="200" %}
```json
{
  "username": 1,
  "socials": {
    "twitter": "",
    "twitch": "",
    "instagram": "",
    "tiktok": ""
  }
}
```
{% endtab %}

{% tab title="401" %}
```json
{
"errorCode": 401,
"message": "unauthorized"
}
```
{% endtab %}
{% endtabs %}
