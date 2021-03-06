# OpenAPI.yml example

```yaml
swagger: '2.0'
info:
  title: tfkparameterinterface.azurewebsites.net
  version: 1.0.0
host: tfkparameterinterface.azurewebsites.net
basePath: /
schemes:
  - https
  - http
paths:
  /api/ParameterInterface:
    post:
      operationId: /api/ParameterInterface/post
      description: Send mail from defined sender and optionally attatchments.
      summary: Send mail
      produces:
        - application/json
      consumes:
        - application/json
      parameters:
        - name: body
          in: body
          description: Parameters for sending mail
          x-ms-summary: Parameters
          x-ms-visibility: important
          required: true
          schema:
            type: object
            properties:
              to:
                description: example@example.com
                type: string
                x-ms-summary: To
                x-ms-visibility: important
              from:
                description: example2@example.com
                type: string
                x-ms-summary: From
                x-ms-visibility: important
              subject:
                description: Subject
                type: string
                x-ms-summary: Subject
                x-ms-visibility: important
              text:
                description: Body
                type: string
                x-ms-summary: Text
                x-ms-visibility: important
              html:
                description: Html in body
                type: string
                x-ms-summary: Html
                x-ms-visibility: advanced
              cc:
                description: example3@example.com
                type: string
                x-ms-summary: CC
                x-ms-visibility: advanced
              bcc:
                description: example4@example.com
                type: string
                x-ms-summary: BCC
                x-ms-visibility: advanced
              replyTo:
                description: E-mail
                type: string
                x-ms-summary: Reply to
                x-ms-visibility: advanced
              attachments:
                description: Array of attachments
                type: array
                items:
                  type: object
                  properties:
                    content:
                      description: Base64 encoded content
                      type: string
                      x-ms-summary: Content
                      x-ms-visibility: important
                    filename:
                      description: example.txt
                      type: string
                      x-ms-summary: Filename
                      x-ms-visibility: important
                    type:
                      description: plain/text
                      type: string
                      x-ms-summary: Type
                      x-ms-visibility: important
                    disposition:
                      description: Disposition
                      type: string
                      x-ms-summary: Disposition
                      x-ms-visibility: advanced
                    content_id:
                      description: Content id
                      type: string
                      x-ms-summary: Content ID
                      x-ms-visibility: advanced
                x-ms-summary: Attachments
                x-ms-visibility: advanced
      responses:
        '200':
          description: Mail sent
          x-ms-summary: Mail sent
      security:
        - apikeyQuery: []
definitions: {}
securityDefinitions:
  apikeyQuery:
    type: apiKey
    name: code
    in: query

```
