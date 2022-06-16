# Fastapi Swagger UI Dark
Dark theme for Swagger UI used in Fastapi applications ([swagger-ui-dist](https://cdn.jsdelivr.net/npm/swagger-ui-dist@4/swagger-ui.css)) based on [catppuccin color theme](https://github.com/catppuccin/catppuccin)


## Usage
You can pass the cdn link to `swagger_css_url` parameter in `get_swagger_ui_html` function in Fastapi

**CDN Link:**
```html
https://cdn.jsdelivr.net/gh/Itz-fork/Fastapi-Swagger-UI-Dark/swagger_ui_dark.css
```

**Example usage:**
```python
@app.get("/docs", include_in_schema=False)
async def custom_swagger_ui_html():
    return get_swagger_ui_html(
        openapi_url=app.openapi_url,
        title=app.title + " - Swagger UI",
        swagger_css_url="https://cdn.jsdelivr.net/gh/Itz-fork/Fastapi-Swagger-UI-Dark/swagger_ui_dark.css"
    )
```
