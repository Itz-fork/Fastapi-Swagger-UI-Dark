# Fastapi Swagger UI Dark
Dark theme for Swagger UI used in Fastapi applications ([swagger-ui-dist](https://cdn.jsdelivr.net/npm/swagger-ui-dist@4/swagger-ui.css)) based on [catppuccin color theme](https://github.com/catppuccin/catppuccin)


## Usage
You can pass the cdn link to `swagger_css_url` parameter in `get_swagger_ui_html` function in Fastapi

> There are 2 css files,
> - [swagger_ui_dark.css](assets/swagger_ui_dark.css) - Main css file
> - [swagger_ui_dark.min.css](assets/swagger_ui_dark.min.css) - Minified version of the 1st one

- **With CDN (jsdelivr)**
    - CDN url:
        ```
        https://cdn.jsdelivr.net/gh/Itz-fork/Fastapi-Swagger-UI-Dark/assets/swagger_ui_dark.min.css
        ```
    - Example:
        ```python
        @app.get("/docs", include_in_schema=False)
        async def custom_swagger_ui_html_cdn():
            return get_swagger_ui_html(
            openapi_url=app.openapi_url,
            title=f"{app.title} - Swagger UI",
            # swagger_ui_dark.css CDN link
            swagger_css_url="https://cdn.jsdelivr.net/gh/Itz-fork/Fastapi-Swagger-UI-Dark/assets/swagger_ui_dark.min.css"
        )
        ```
- **With Github**
    - Raw url:
        ```
        https://raw.githubusercontent.com/Itz-fork/Fastapi-Swagger-UI-Dark/main/assets/swagger_ui_dark.min.css
        ```
    - Example:
        ```python
        @app.get("/docs", include_in_schema=False)
        async def custom_swagger_ui_html_github():
            return get_swagger_ui_html(
            openapi_url=app.openapi_url,
            title=f"{app.title} - Swagger UI",
            # swagger_ui_dark.css raw url
            swagger_css_url="https://raw.githubusercontent.com/Itz-fork/Fastapi-Swagger-UI-Dark/main/assets/swagger_ui_dark.min.css"
        )
        ```