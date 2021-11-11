## NEED HELP?

Email at eaidter@gmail.com to hire us with minimal cost.

## templates/search.liquid
Hide product or/and content in search results when customer uses the search feature on the website. 

### HIDE PRODUCT
Add the following below the line `{% for item in search.results %}` and before the closing `{% endfor %}`

    {% assign tags = item.tags | join:', ' | downcase %}
    {% unless tags contains 'search hide' %}

        // search result

    {% endunless %}

### HIDE URL - BLOG / PAGE
Locate family code that contain for page results. Example: `{{ 'general.search.pages_and_articles' | t }}`

Add the following below the line `{% for item in search.results %}` and before the closing `{% endfor %}`

    {% unless item.url contains 'url-name' %}

     // search result

    {% endunless %}
