# Fastapi Swagger UI Dark
Dark theme for Swagger UI used in Fastapi applications ([swagger-ui-dist](https://cdn.jsdelivr.net/npm/swagger-ui-dist@4/swagger-ui.css)) based on [catppuccin color theme](https://github.com/catppuccin/catppuccin)


## Usage
You can pass the cdn link to `swagger_css_url` parameter in `get_swagger_ui_html` function in Fastapi

- **With CDN (jsdelivr)**
    - CDN url:
        ```
        https://cdn.jsdelivr.net/gh/Itz-fork/Fastapi-Swagger-UI-Dark/swagger_ui_dark.css
        ```
    - Example:
        ```python
        @app.get("/docs", include_in_schema=False)
        async def custom_swagger_ui_html_cdn():
            return get_swagger_ui_html(
            openapi_url=app.openapi_url,
            title=f"{app.title} - Swagger UI",
            # swagger_ui_dark.css CDN link
            swagger_css_url="https://cdn.jsdelivr.net/gh/Itz-fork/Fastapi-Swagger-UI-Dark/swagger_ui_dark.css"
        )
        ```
- **With Github**
    - Raw url:
        ```
        https://raw.githubusercontent.com/Itz-fork/Fastapi-Swagger-UI-Dark/main/swagger_ui_dark.css
        ```
    - Example:
        ```python
        @app.get("/docs", include_in_schema=False)
        async def custom_swagger_ui_html_github():
            return get_swagger_ui_html(
            openapi_url=app.openapi_url,
            title=f"{app.title} - Swagger UI",
            # swagger_ui_dark.css raw url
            swagger_css_url="https://raw.githubusercontent.com/Itz-fork/Fastapi-Swagger-UI-Dark/main/swagger_ui_dark.css"
        )
        ```