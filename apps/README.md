```
openapi: 3.1.0
info:
  title: rc_app_api
  version: '1.0'
servers:
  - url: '[url]/api/apps'
    description: URL of RC Server
paths:
  '/{id}/settings/{setting-id}':
    parameters:
      - schema:
          type: string
        name: id
        in: path
        required: true
        description: Id of the App.
      - schema:
          type: string
        name: setting-id
        in: path
        required: true
        description: Id of the target Setting.
    get:
      summary: getSetting
      tags:
        - app
        - setting
        - general
      responses:
        '200':
          description: OK
          content:
            application/json:
              schema:
                description: ''
                type: object
                x-examples:
                  example-1:
                    setting:
                      id: log_level
                      public: true
                      type: select
                      packageValue: '0'
                      value: '2'
                      values:
                        - key: '0'
                          i18nLabel: 0_Errors_Only
                        - key: '1'
                          i18nLabel: 1_Errors_and_Information
                        - key: '2'
                          i18nLabel: 2_Erros_Information_and_Debug
                      i18nLabel: dialogflow_log_level
                      i18nDescription: dialogflow_log_level_description
                      required: false
                      createdAt: '2021-11-29T17:46:17.363Z'
                      updatedAt: '2021-11-30T14:15:07.345Z'
                    success: true
                properties:
                  setting:
                    type: object
                  success:
                    type: boolean
                required:
                  - setting
                  - success
              examples:
                app setting example:
                  value:
                    setting:
                      id: log_level
                      public: true
                      type: select
                      packageValue: '0'
                      value: '2'
                      values:
                        - key: '0'
                          i18nLabel: 0_Errors_Only
                        - key: '1'
                          i18nLabel: 1_Errors_and_Information
                        - key: '2'
                          i18nLabel: 2_Erros_Information_and_Debug
                      i18nLabel: dialogflow_log_level
                      i18nDescription: dialogflow_log_level_description
                      required: false
                      createdAt: '2021-11-29T17:46:17.363Z'
                      updatedAt: '2021-11-30T14:15:07.345Z'
                    success: true
                agent list setting example:
                  value:
                    setting:
                      id: agents
                      public: true
                      type: multiCode
                      packageValue: "[\n\t{\n\t\t\"omnichannel_agent\": {\n\t\t\t\"project_id\": \"\",\n\t\t\t\"client_email\": \"\",\n\t\t\t\"agent_id\": \"\",\n\t\t\t\"agent_region\": \"\",\n\t\t\t\"agent_default_language\": \"EN\",\n\t\t\t\"environment_id\": \"\",\n\t\t\t\"private_key\": \"\",\n\t\t\t\"agent_version\": \"\",\n\t\t\t\"fallback_responses_limit\": 3,\n\t\t\t\"fallback_target_department\": \"Viasat Customer Support\",\n\t\t\t\"handover_message\": \"Connecting you with a live agent\",\n\t\t\t\"no_agents_for_handover_message\": \"\",\n\t\t\t\"service_unavailable_message\": \"There are no agents currently available. Our Customer Care team is available by phone 24/7 at 1-855-463-9333.\",\n\t\t\t\"close_chat_message\": \"Thanks for contacting Viasat Customer Care. We appreciate your business. Please close this window to end your chat session.\",\n\t\t\t\"hide_quickreplies\": true,\n\t\t\t\"enable_chat_closed_by_visitor_event\": true,\n\t\t\t\"chat_closed_by_visitor_event\": \"end_live_chat\",\n\t\t\t\"enable_welcome_message\": true,\n\t\t\t\"welcome_message\": \"Hi there! I am a virtual assistant, designed to answer questions about your service.\",\n\t\t\t\"welcome_intent_on_start\": true,\n\t\t\t\"enable_customer_timeout\": false,\n\t\t\t\"customer_timeout_time\": 240,\n\t\t\t\"customer_timeout_warning_time\": 180,\n\t\t\t\"customer_timeout_warning_message\": \"Are you still there? Please send a message within %t or this chat will time out.\",\n\t\t\t\"session_maintenance_interval\": \"5 minutes\",\n\t\t\t\"session_maintenance_event_name\": \"session_maintenance\"\n\t\t}\n\t}\n]"
                      i18nLabel: dialogflow_bot_list_config
                      i18nDescription: dialogflow_bot_list_config_description
                      required: true
                      createdAt: '2021-11-30T14:34:36.178Z'
                      updatedAt: '2021-12-06T13:00:12.629Z'
                      value: "[\n\t{\n\t\t\"omnichannel_agent\": {\n\t\t\t\"project_id\": \"\",\n\t\t\t\"client_email\": \"\",\n\t\t\t\"agent_id\": \"\",\n\t\t\t\"agent_region\": \"\",\n\t\t\t\"agent_default_language\": \"EN\",\n\t\t\t\"environment_id\": \"\",\n\t\t\t\"private_key\": \"\",\n\t\t\t\"agent_version\": \"\",\n\t\t\t\"fallback_responses_limit\": 3,\n\t\t\t\"fallback_target_department\": \"Viasat Customer Support\",\n\t\t\t\"handover_message\": \"Connecting you with a live agent\",\n\t\t\t\"no_agents_for_handover_message\": \"\",\n\t\t\t\"service_unavailable_message\": \"There are no agents currently available. Our Customer Care team is available by phone 24/7 at 1-855-463-9333.\",\n\t\t\t\"close_chat_message\": \"Thanks for contacting Viasat Customer Care. We appreciate your business. Please close this window to end your chat session.\",\n\t\t\t\"hide_quickreplies\": true,\n\t\t\t\"enable_chat_closed_by_visitor_event\": true,\n\t\t\t\"chat_closed_by_visitor_event\": \"end_live_chat\",\n\t\t\t\"enable_welcome_message\": true,\n\t\t\t\"welcome_message\": \"Hi there! I am a virtual assistant, designed to answer questions about your service.\",\n\t\t\t\"welcome_intent_on_start\": true,\n\t\t\t\"enable_customer_timeout\": false,\n\t\t\t\"customer_timeout_time\": 240,\n\t\t\t\"customer_timeout_warning_time\": 180,\n\t\t\t\"customer_timeout_warning_message\": \"Are you still there? Please send a message within %t or this chat will time out.\",\n\t\t\t\"session_maintenance_interval\": \"5 minutes\",\n\t\t\t\"session_maintenance_event_name\": \"session_maintenance\"\n\t\t}\n\t},\n\t{\n\t\t\"test_agent\": {\n\t\t\t\"project_id\": \"2\",\n\t\t\t\"client_email\": \"\",\n\t\t\t\"agent_id\": \"\",\n\t\t\t\"agent_region\": \"\",\n\t\t\t\"agent_default_language\": \"EN\",\n\t\t\t\"environment_id\": \"\",\n\t\t\t\"private_key\": \"\",\n\t\t\t\"agent_version\": \"\",\n\t\t\t\"fallback_responses_limit\": 3,\n\t\t\t\"fallback_target_department\": \"Viasat Customer Support\",\n\t\t\t\"handover_message\": \"Connecting you with a live agent\",\n\t\t\t\"no_agents_for_handover_message\": \"\",\n\t\t\t\"service_unavailable_message\": \"There are no agents currently available. Our Customer Care team is available by phone 24/7 at 1-855-463-9333.\",\n\t\t\t\"close_chat_message\": \"Thanks for contacting Viasat Customer Care. We appreciate your business. Please close this window to end your chat session.\",\n\t\t\t\"hide_quickreplies\": true,\n\t\t\t\"enable_chat_closed_by_visitor_event\": true,\n\t\t\t\"chat_closed_by_visitor_event\": \"end_live_chat\",\n\t\t\t\"enable_welcome_message\": true,\n\t\t\t\"welcome_message\": \"Hi there! I am a virtual assistant, designed to answer questions about your service.\",\n\t\t\t\"welcome_intent_on_start\": true,\n\t\t\t\"enable_customer_timeout\": false,\n\t\t\t\"customer_timeout_time\": 240,\n\t\t\t\"customer_timeout_warning_time\": 180,\n\t\t\t\"customer_timeout_warning_message\": \"Are you still there? Please send a message within %t or this chat will time out.\",\n\t\t\t\"session_maintenance_interval\": \"5 minutes\",\n\t\t\t\"session_maintenance_event_name\": \"session_maintenance\"\n\t\t}\n\t}\n]"
                    success: true
            application/xml:
              schema:
                type: object
                properties: {}
        '404':
          description: Not Found
          content:
            application/json:
              schema:
                description: ''
                type: object
                properties:
                  success:
                    type: boolean
                  error:
                    type: string
                    minLength: 1
                required:
                  - success
                  - error
                x-examples:
                  example-1:
                    success: false
                    error: No value in request body
              examples:
                No Setting found:
                  value:
                    success: false
                    error: 'No Setting found on the App by the id of: {id}'
                No App found:
                  value:
                    success: false
                    error: 'No App found by the id of: {id}'
      operationId: get-id-settings-settingId-'
      parameters: []
      description: |-
        Returns and Updates the value of Setting with the specified setting-id on the App with the specified id

        --- FOR setting-id === 'agents'---

        This setting-id returns the setting object handling all agent settings. The property "value" of the object is a JSON file with a list of agents containing agent settings.
    post:
      summary: updateSetting
      tags:
        - app
        - setting
        - general
      responses:
        '200':
          description: OK
          content:
            application/json:
              schema:
                description: ''
                type: object
                properties:
                  sucess:
                    type: boolean
                required:
                  - sucess
                x-examples:
                  example-1:
                    sucess: true
              examples:
                post app setting loglevel:
                  value:
                    success: true
        '400':
          description: Bad Request
          content:
            application/json:
              schema:
                description: ''
                type: object
                properties:
                  success:
                    type: boolean
                  error:
                    type: string
                    minLength: 1
                required:
                  - success
                  - error
                x-examples:
                  example-1:
                    success: false
                    error: No value in request body
              examples:
                No value in request body:
                  value:
                    success: false
                    error: No value in request body
        '404':
          description: Not Found
          content:
            application/json:
              schema:
                description: ''
                type: object
                properties:
                  success:
                    type: boolean
                  error:
                    type: string
                    minLength: 1
                required:
                  - success
                  - error
                x-examples:
                  example-1:
                    success: false
                    error: 'No Setting found on the App by the id of: "log_levesl"'
              examples:
                No Setting found:
                  value:
                    success: false
                    error: 'No Setting found on the App by the id of: {id}'
                No App found:
                  value:
                    success: false
                    error: 'No App by the id of: {id}'
      operationId: post-id-settings-settingId-'
      parameters: []
      requestBody:
        content:
          application/json:
            schema:
              description: ''
              type: object
              x-examples:
                example-1:
                  value: {}
              properties:
                value:
                  type:
                    - boolean
                    - integer
                    - array
                    - string
                  items: {}
              required:
                - value
            examples:
              Setting Example:
                value:
                  value: any
              Agent list Example:
                value:
                  value: '[ { "omnichannel_agent": { "project_id": "", "client_email": "", "agent_id": "", "agent_region": "", "agent_default_language": "EN", "environment_id": "", "private_key": "", "agent_version": "", "fallback_responses_limit": 3, "fallback_target_department": "Viasat Customer Support", "handover_message": "Connecting you with a live agent", "no_agents_for_handover_message": "", "service_unavailable_message":"", "close_chat_message": "Thanks for contacting Viasat Customer Care. We appreciate your business. Please close this window to end your chat session.", "hide _quickreplies": true, "enable_chat_closed_by_visitor_event": true, "chat_closed_by_visitor_event": "end_live_chat", "enable_welcome_message": true, "welcome_message": "Hi there! I am a virtual assistant, designed to answer questions about your service.", "welcome_intent_on_start": true, "enable_customer_timeout": false, "customer_timeout_time": 240, "customer_timeout_warning_time": 180, "customer_timeout_warning_message": "Are you still there? Please send a message within %t or this chat will time out.", "session_maintenance_interval": "5 minutes", "session_maintenance_event_name": "session_maintenance" } }, { "test_agent": { "project_id": "2", "client_email": "", "agent_id": "", "agent_region": "", "agent_default_language": "EN", "environment_id": "", "private_key": "", "agent_version": "", "fallback_responses_limit": 3, "fallback_target_department": "Viasat Customer Support", "handover_message": "Connecting you with a live agent", "no_agents_for_handover_message": "", "service_unavailable_message":"", "close_chat_message":"Thanks for contacting Viasat Customer Care. We appreciate your business. Please close this window to end your chat session.", "hide_quickreplies": true, "enable_chat_closed_by_visitor_event": true, "chat_closed_by_visitor_event": "end_live_chat", "enable_welcome_message": true, "welcome_message": "Hi there! I am a virtual assistant, designed to answer questions about your service.", "welcome_intent_on_start": true, "enable_customer_timeout": false, "customer_timeout_time": 240,"customer_timeout_warning_time": 180,"customer_timeout_warning_message": "Are you still there? Please send a message within %t or this chat will time out.", "session_maintenance_interval": "5 minutes", "session_maintenance_event_name":"session_maintenance" } } ]'
      description: |-
        --- FOR setting-id === 'agents'---

        This setting-id updates the value of the setting object handling all agent settings.

        Any update from this endpoint will reset the entire JSON list. It is not recommended in the case only a single agent needs to be updated
  '/{id}/settings/{setting-id}/{agent-name}':
    parameters:
      - schema:
          type: string
        name: id
        in: path
        required: true
        description: Id of the App.
      - schema:
          type: string
        name: setting-id
        in: path
        required: true
        description: Id of the target Setting.
      - schema:
          type: string
        name: agent-name
        in: path
        required: true
        description: Username of the Agent.
    get:
      summary: getAgentConfig
      tags:
        - app
        - setting
        - general
        - multiagent
      responses:
        '200':
          description: OK
          content:
            application/json:
              schema:
                description: ''
                type: object
                properties:
                  agentConfig:
                    type: object
                    properties:
                      project_id:
                        type: string
                        minLength: 1
                      client_email:
                        type: string
                      agent_id:
                        type: string
                      agent_region:
                        type: string
                      agent_default_language:
                        type: string
                        minLength: 1
                      environment_id:
                        type: string
                      private_key:
                        type: string
                      agent_version:
                        type: string
                      fallback_responses_limit:
                        type: number
                      fallback_target_department:
                        type: string
                        minLength: 1
                      handover_message:
                        type: string
                        minLength: 1
                      no_agents_for_handover_message:
                        type: string
                      service_unavailable_message:
                        type: string
                        minLength: 1
                      close_chat_message:
                        type: string
                        minLength: 1
                      hide_quickreplies:
                        type: boolean
                      enable_chat_closed_by_visitor_event:
                        type: boolean
                      chat_closed_by_visitor_event:
                        type: string
                        minLength: 1
                      enable_welcome_message:
                        type: boolean
                      welcome_message:
                        type: string
                        minLength: 1
                      welcome_intent_on_start:
                        type: boolean
                      enable_customer_timeout:
                        type: boolean
                      customer_timeout_time:
                        type: number
                      customer_timeout_warning_time:
                        type: number
                      customer_timeout_warning_message:
                        type: string
                        minLength: 1
                      session_maintenance_interval:
                        type: string
                        minLength: 1
                      session_maintenance_event_name:
                        type: string
                        minLength: 1
                    required:
                      - project_id
                      - client_email
                      - agent_id
                      - agent_region
                      - agent_default_language
                      - environment_id
                      - private_key
                      - agent_version
                      - fallback_responses_limit
                      - fallback_target_department
                      - handover_message
                      - no_agents_for_handover_message
                      - service_unavailable_message
                      - close_chat_message
                      - hide_quickreplies
                      - enable_chat_closed_by_visitor_event
                      - chat_closed_by_visitor_event
                      - enable_welcome_message
                      - welcome_message
                      - welcome_intent_on_start
                      - enable_customer_timeout
                      - customer_timeout_time
                      - customer_timeout_warning_time
                      - customer_timeout_warning_message
                      - session_maintenance_interval
                      - session_maintenance_event_name
                  success:
                    type: boolean
                required:
                  - agentConfig
                  - success
                x-examples:
                  example-1:
                    agentConfig:
                      project_id: '2'
                      client_email: ''
                      agent_id: ''
                      agent_region: ''
                      agent_default_language: EN
                      environment_id: ''
                      private_key: ''
                      agent_version: ''
                      fallback_responses_limit: 3
                      fallback_target_department: Viasat Customer Support
                      handover_message: Connecting you with a live agent
                      no_agents_for_handover_message: ''
                      service_unavailable_message: There are no agents currently available. Our Customer Care team is available by phone 24/7 at 1-855-463-9333.
                      close_chat_message: Thanks for contacting Viasat Customer Care. We appreciate your business. Please close this window to end your chat session.
                      hide_quickreplies: true
                      enable_chat_closed_by_visitor_event: true
                      chat_closed_by_visitor_event: end_live_chat
                      enable_welcome_message: true
                      welcome_message: 'Hi there! I am a virtual assistant, designed to answer questions about your service.'
                      welcome_intent_on_start: true
                      enable_customer_timeout: false
                      customer_timeout_time: 240
                      customer_timeout_warning_time: 180
                      customer_timeout_warning_message: Are you still there? Please send a message within %t or this chat will time out.
                      session_maintenance_interval: 5 minutes
                      session_maintenance_event_name: session_maintenance
                    success: true
              examples:
                agent_example:
                  value:
                    agentConfig:
                      project_id: '2'
                      client_email: ''
                      agent_id: ''
                      agent_region: ''
                      agent_default_language: EN
                      environment_id: ''
                      private_key: ''
                      agent_version: ''
                      fallback_responses_limit: 3
                      fallback_target_department: Viasat Customer Support
                      handover_message: Connecting you with a live agent
                      no_agents_for_handover_message: ''
                      service_unavailable_message: There are no agents currently available. Our Customer Care team is available by phone 24/7 at 1-855-463-9333.
                      close_chat_message: Thanks for contacting Viasat Customer Care. We appreciate your business. Please close this window to end your chat session.
                      hide_quickreplies: true
                      enable_chat_closed_by_visitor_event: true
                      chat_closed_by_visitor_event: end_live_chat
                      enable_welcome_message: true
                      welcome_message: 'Hi there! I am a virtual assistant, designed to answer questions about your service.'
                      welcome_intent_on_start: true
                      enable_customer_timeout: false
                      customer_timeout_time: 240
                      customer_timeout_warning_time: 180
                      customer_timeout_warning_message: Are you still there? Please send a message within %t or this chat will time out.
                      session_maintenance_interval: 5 minutes
                      session_maintenance_event_name: session_maintenance
                    success: true
        '404':
          description: Not Found
          content:
            application/json:
              schema:
                description: ''
                type: object
                properties:
                  success:
                    type: boolean
                  error:
                    type: string
                    minLength: 1
                required:
                  - success
                  - error
                x-examples:
                  example-1:
                    success: false
                    error: 'No App found by the id of: 21b7d3nba-031b-41d9-8ff2-fbbfa081ae90'
              examples:
                No App Found:
                  value:
                    success: false
                    error: 'No App found by the id of: {appId}'
                No Setting Sound:
                  value:
                    success: false
                    error: 'No Setting found on the App by the id of: {settingId}'
                No Agent Found:
                  value:
                    success: false
                    error: 'Error: No agent found with name {agent}'
      operationId: get-id-settings-settingId-agentName'
      parameters: []
      description: |
        Returns, adds, updates and deletes agents using an agent-name in the setting with the specified setting-id in App with the specified id.
    post:
      summary: addAgentConfig
      tags:
        - app
        - setting
        - general
        - multiagent
      responses:
        '200':
          description: OK
          content:
            application/json:
              schema:
                description: ''
                type: object
                properties:
                  success:
                    type: boolean
                required:
                  - success
                x-examples:
                  example-1:
                    success: false
              examples:
                Post Agent Success:
                  value:
                    success: true
        '400':
          description: Bad Request
          content:
            application/json:
              schema:
                description: ''
                type: object
                properties:
                  success:
                    type: boolean
                  error:
                    type: string
                    minLength: 1
                required:
                  - success
                  - error
                x-examples:
                  example-1:
                    success: false
                    error: 'No Setting found on the App by the id of: {settingId}'
              examples:
                No value:
                  value:
                    success: true
                    error: No value in request body
        '404':
          description: Not Found
          headers: {}
          content:
            application/json:
              schema:
                description: ''
                type: object
                properties:
                  success:
                    type: boolean
                  error:
                    type: string
                    minLength: 1
                required:
                  - success
                  - error
                x-examples:
                  example-1:
                    success: false
                    error: 'No App found by the id of: {agentId}'
              examples:
                No App Found:
                  value:
                    success: false
                    error: 'No App found by the id of: {appId}'
                No Setting Found:
                  value:
                    success: false
                    error: 'No Setting found on the App by the id of: {settingId}'
                No Agent Found:
                  value:
                    success: false
                    error: 'No Agent found with the name: {agent}'
            application/xml:
              schema:
                type: object
                properties: {}
            multipart/form-data:
              schema:
                type: object
                properties: {}
      operationId: post-id-settings-settingId-agentName'
      requestBody:
        content:
          application/json:
            schema:
              description: ''
              type: object
              properties:
                value:
                  type: object
                  properties:
                    project_id:
                      type: string
                      minLength: 1
                    client_email:
                      type: string
                    agent_id:
                      type: string
                    agent_region:
                      type: string
                    agent_default_language:
                      type: string
                      minLength: 1
                    environment_id:
                      type: string
                    private_key:
                      type: string
                    agent_version:
                      type: string
                    fallback_responses_limit:
                      type: number
                    fallback_target_department:
                      type: string
                      minLength: 1
                    handover_message:
                      type: string
                      minLength: 1
                    no_agents_for_handover_message:
                      type: string
                    service_unavailable_message:
                      type: string
                      minLength: 1
                    close_chat_message:
                      type: string
                      minLength: 1
                    hide_quickreplies:
                      type: boolean
                    enable_chat_closed_by_visitor_event:
                      type: boolean
                    chat_closed_by_visitor_event:
                      type: string
                      minLength: 1
                    enable_welcome_message:
                      type: boolean
                    welcome_message:
                      type: string
                      minLength: 1
                    welcome_intent_on_start:
                      type: boolean
                    enable_customer_timeout:
                      type: boolean
                    customer_timeout_time:
                      type: number
                    customer_timeout_warning_time:
                      type: number
                    customer_timeout_warning_message:
                      type: string
                      minLength: 1
                    session_maintenance_interval:
                      type: string
                      minLength: 1
                    session_maintenance_event_name:
                      type: string
                      minLength: 1
                  required:
                    - project_id
                    - client_email
                    - agent_id
                    - agent_region
                    - agent_default_language
                    - environment_id
                    - private_key
                    - agent_version
                    - fallback_responses_limit
                    - fallback_target_department
                    - handover_message
                    - no_agents_for_handover_message
                    - service_unavailable_message
                    - close_chat_message
                    - hide_quickreplies
                    - enable_chat_closed_by_visitor_event
                    - chat_closed_by_visitor_event
                    - enable_welcome_message
                    - welcome_message
                    - welcome_intent_on_start
                    - enable_customer_timeout
                    - customer_timeout_time
                    - customer_timeout_warning_time
                    - customer_timeout_warning_message
                    - session_maintenance_interval
                    - session_maintenance_event_name
              required:
                - value
              x-examples:
                example-1:
                  value:
                    project_id: '2'
                    client_email: ''
                    agent_id: ''
                    agent_region: ''
                    agent_default_language: EN
                    environment_id: ''
                    private_key: ''
                    agent_version: ''
                    fallback_responses_limit: 3
                    fallback_target_department: Viasat Customer Support
                    handover_message: Connecting you with a live agent
                    no_agents_for_handover_message: ''
                    service_unavailable_message: There are no agents currently available. Our Customer Care team is available by phone 24/7 at 1-855-463-9333.
                    close_chat_message: Thanks for contacting Viasat Customer Care. We appreciate your business. Please close this window to end your chat session.
                    hide_quickreplies: true
                    enable_chat_closed_by_visitor_event: true
                    chat_closed_by_visitor_event: end_live_chat
                    enable_welcome_message: true
                    welcome_message: 'Hi there! I am a virtual assistant, designed to answer questions about your service.'
                    welcome_intent_on_start: true
                    enable_customer_timeout: false
                    customer_timeout_time: 240
                    customer_timeout_warning_time: 180
                    customer_timeout_warning_message: Are you still there? Please send a message within %t or this chat will time out.
                    session_maintenance_interval: 5 minutes
                    session_maintenance_event_name: session_maintenance
            examples:
              Agent Example:
                value:
                  value:
                    project_id: '2'
                    client_email: ''
                    agent_id: ''
                    agent_region: ''
                    agent_default_language: EN
                    environment_id: ''
                    private_key: ''
                    agent_version: ''
                    fallback_responses_limit: 3
                    fallback_target_department: Viasat Customer Support
                    handover_message: Connecting you with a live agent
                    no_agents_for_handover_message: ''
                    service_unavailable_message: There are no agents currently available. Our Customer Care team is available by phone 24/7 at 1-855-463-9333.
                    close_chat_message: Thanks for contacting Viasat Customer Care. We appreciate your business. Please close this window to end your chat session.
                    hide_quickreplies: true
                    enable_chat_closed_by_visitor_event: true
                    chat_closed_by_visitor_event: end_live_chat
                    enable_welcome_message: true
                    welcome_message: 'Hi there! I am a virtual assistant, designed to answer questions about your service.'
                    welcome_intent_on_start: true
                    enable_customer_timeout: false
                    customer_timeout_time: 240
                    customer_timeout_warning_time: 180
                    customer_timeout_warning_message: Are you still there? Please send a message within %t or this chat will time out.
                    session_maintenance_interval: 5 minutes
                    session_maintenance_event_name: session_maintenance
    put:
      summary: updateAgentConfig
      tags:
        - app
        - setting
        - general
        - multiagent
      responses:
        '200':
          description: OK
          content:
            application/json:
              schema:
                description: ''
                type: object
                properties:
                  sucess:
                    type: boolean
                required:
                  - sucess
                x-examples:
                  example-1:
                    sucess: true
              examples:
                Agent Update Success:
                  value:
                    sucess: true
        '400':
          description: Bad Request
          content:
            application/json:
              schema:
                description: ''
                type: object
                properties:
                  success:
                    type: boolean
                  error:
                    type: string
                    minLength: 1
                required:
                  - success
                  - error
                x-examples:
                  example-1:
                    success: false
                    error: No value in request body
              examples:
                No value:
                  value:
                    success: false
                    error: No value in request body
        '404':
          description: Not Found
          content:
            application/json:
              schema:
                description: ''
                type: object
                properties:
                  success:
                    type: boolean
                  error:
                    type: string
                    minLength: 1
                required:
                  - success
                  - error
                x-examples:
                  example-1:
                    success: false
                    error: 'No Setting found on the App by the id of: {settingId}'
              examples:
                No App Found:
                  value:
                    success: false
                    error: 'No App found by the id of: {appId}'
                No Setting Found:
                  value:
                    success: false
                    error: 'No Setting found on the App by the id of: {settingId}'
                No Agent Found:
                  value:
                    success: false
                    error: 'No Agent found with the name: {agent}'
      operationId: put-id-settings-settingId-agentName'
      requestBody:
        content:
          application/json:
            schema:
              description: ''
              type: object
              properties:
                value:
                  type: object
                  properties:
                    project_id:
                      type: string
                      minLength: 1
                    client_email:
                      type: string
                    agent_id:
                      type: string
                    agent_region:
                      type: string
                    agent_default_language:
                      type: string
                      minLength: 1
                    environment_id:
                      type: string
                    private_key:
                      type: string
                    agent_version:
                      type: string
                    fallback_responses_limit:
                      type: number
                    fallback_target_department:
                      type: string
                      minLength: 1
                    handover_message:
                      type: string
                      minLength: 1
                    no_agents_for_handover_message:
                      type: string
                    service_unavailable_message:
                      type: string
                      minLength: 1
                    close_chat_message:
                      type: string
                      minLength: 1
                    hide_quickreplies:
                      type: boolean
                    enable_chat_closed_by_visitor_event:
                      type: boolean
                    chat_closed_by_visitor_event:
                      type: string
                      minLength: 1
                    enable_welcome_message:
                      type: boolean
                    welcome_message:
                      type: string
                      minLength: 1
                    welcome_intent_on_start:
                      type: boolean
                    enable_customer_timeout:
                      type: boolean
                    customer_timeout_time:
                      type: number
                    customer_timeout_warning_time:
                      type: number
                    customer_timeout_warning_message:
                      type: string
                      minLength: 1
                    session_maintenance_interval:
                      type: string
                      minLength: 1
                    session_maintenance_event_name:
                      type: string
                      minLength: 1
                  required:
                    - project_id
                    - client_email
                    - agent_id
                    - agent_region
                    - agent_default_language
                    - environment_id
                    - private_key
                    - agent_version
                    - fallback_responses_limit
                    - fallback_target_department
                    - handover_message
                    - no_agents_for_handover_message
                    - service_unavailable_message
                    - close_chat_message
                    - hide_quickreplies
                    - enable_chat_closed_by_visitor_event
                    - chat_closed_by_visitor_event
                    - enable_welcome_message
                    - welcome_message
                    - welcome_intent_on_start
                    - enable_customer_timeout
                    - customer_timeout_time
                    - customer_timeout_warning_time
                    - customer_timeout_warning_message
                    - session_maintenance_interval
                    - session_maintenance_event_name
              required:
                - value
              x-examples:
                example-1:
                  value:
                    project_id: '2'
                    client_email: ''
                    agent_id: ''
                    agent_region: ''
                    agent_default_language: EN
                    environment_id: ''
                    private_key: ''
                    agent_version: ''
                    fallback_responses_limit: 3
                    fallback_target_department: Viasat Customer Support
                    handover_message: Connecting you with a live agent
                    no_agents_for_handover_message: ''
                    service_unavailable_message: There are no agents currently available. Our Customer Care team is available by phone 24/7 at 1-855-463-9333.
                    close_chat_message: Thanks for contacting Viasat Customer Care. We appreciate your business. Please close this window to end your chat session.
                    hide_quickreplies: true
                    enable_chat_closed_by_visitor_event: true
                    chat_closed_by_visitor_event: end_live_chat
                    enable_welcome_message: true
                    welcome_message: 'Hi there! I am a virtual assistant, designed to answer questions about your service.'
                    welcome_intent_on_start: true
                    enable_customer_timeout: false
                    customer_timeout_time: 240
                    customer_timeout_warning_time: 180
                    customer_timeout_warning_message: Are you still there? Please send a message within %t or this chat will time out.
                    session_maintenance_interval: 5 minutes
                    session_maintenance_event_name: session_maintenance
            examples:
              Agent Example:
                value:
                  value:
                    project_id: '2'
                    client_email: ''
                    agent_id: ''
                    agent_region: ''
                    agent_default_language: EN
                    environment_id: ''
                    private_key: ''
                    agent_version: ''
                    fallback_responses_limit: 3
                    fallback_target_department: Viasat Customer Support
                    handover_message: Connecting you with a live agent
                    no_agents_for_handover_message: ''
                    service_unavailable_message: There are no agents currently available. Our Customer Care team is available by phone 24/7 at 1-855-463-9333.
                    close_chat_message: Thanks for contacting Viasat Customer Care. We appreciate your business. Please close this window to end your chat session.
                    hide_quickreplies: true
                    enable_chat_closed_by_visitor_event: true
                    chat_closed_by_visitor_event: end_live_chat
                    enable_welcome_message: true
                    welcome_message: 'Hi there! I am a virtual assistant, designed to answer questions about your service.'
                    welcome_intent_on_start: true
                    enable_customer_timeout: false
                    customer_timeout_time: 240
                    customer_timeout_warning_time: 180
                    customer_timeout_warning_message: Are you still there? Please send a message within %t or this chat will time out.
                    session_maintenance_interval: 5 minutes
                    session_maintenance_event_name: session_maintenance
    delete:
      summary: deleteAgentConfig
      tags:
        - app
        - setting
        - general
        - multiagent
      responses:
        '200':
          description: OK
          content:
            application/json:
              schema:
                description: ''
                type: object
                properties:
                  success:
                    type: boolean
                required:
                  - success
                x-examples:
                  example-1:
                    success: false
              examples:
                Agent Delete Success:
                  value:
                    success: true
        '404':
          description: Not Found
          content:
            application/json:
              schema:
                description: ''
                type: object
                properties:
                  success:
                    type: boolean
                  error:
                    type: string
                    minLength: 1
                required:
                  - success
                  - error
                x-examples:
                  example-1:
                    success: false
                    error: 'No Setting found on the App by the id of: {settingId}'
              examples:
                No App Found:
                  value:
                    success: false
                    error: 'No App found by the id of: {appId}'
                No Setting Found:
                  value:
                    success: false
                    error: 'No Setting found on the App by the id of: {settingId}'
                No Agent Found:
                  value:
                    success: false
                    error: 'No Agent found with the name: {agent}'
      operationId: delete-id-settings-settingId-agentName'
  /'':
    get:
      summary: getApps
      tags:
        - apps
        - general
        - query params
      responses:
        '200':
          description: OK
          content:
            application/json:
              schema:
                description: ''
                type: object
                properties:
                  apps:
                    type: array
                    uniqueItems: true
                    minItems: 1
                    items:
                      required:
                        - id
                        - version
                        - requiredApiVersion
                        - iconFile
                        - name
                        - nameSlug
                        - classFile
                        - description
                        - commitHash
                        - iconFileContent
                        - updatedAt
                        - status
                      properties:
                        id:
                          type: string
                          minLength: 1
                        version:
                          type: string
                          minLength: 1
                        requiredApiVersion:
                          type: string
                          minLength: 1
                        iconFile:
                          type: string
                          minLength: 1
                        author:
                          type: object
                          properties:
                            name:
                              type: string
                              minLength: 1
                            homepage:
                              type: string
                              minLength: 1
                            support:
                              type: string
                              minLength: 1
                          required:
                            - name
                            - homepage
                            - support
                        name:
                          type: string
                          minLength: 1
                        nameSlug:
                          type: string
                          minLength: 1
                        classFile:
                          type: string
                          minLength: 1
                        description:
                          type: string
                          minLength: 1
                        implements:
                          type: array
                          items:
                            required: []
                            properties: {}
                        commitHash:
                          type: string
                          minLength: 1
                        iconFileContent:
                          type: string
                          minLength: 1
                        updatedAt:
                          type: string
                          minLength: 1
                        status:
                          type: string
                          minLength: 1
                        languages:
                          type: object
                          properties: {}
                          required: []
                  success:
                    type: boolean
                required:
                  - apps
                  - success
                x-examples:
                  example-1:
                    apps:
                      - id: 0d3ac5b3-dd0b-43d3-924a-5a7433902589
                        version: 1.0.0
                        requiredApiVersion: ^1.17.0
                        iconFile: icon.png
                        author:
                          name: Rocket.Chat
                          homepage: 'https://github.com/RocketChat/Apps.Salesforce.LiveAgent'
                          support: 'https://github.com/RocketChat/Apps.Salesforce.LiveAgent/issues'
                        name: Saleforce Live Agent Integration
                        nameSlug: salesforce-live-agent-integration
                        classFile: SalesforceLiveAgentApp.js
                        description: Integration between Rocket.Chat and the Salesforce Live Agent (Chat). Please refer our Github repository for setup instructions.
                        implements:
                          - IPostMessageSent
                          - IPostLivechatAgentAssigned
                          - IPostLivechatAgentUnassigned
                          - IPostLivechatRoomClosed
                          - IRoomUserTyping
                          - IUIKitLivechatInteractionHandler
                        commitHash: 947b904c7e5fe7512fb0d7df174a2ffc0ee02397
                        iconFileContent: 'data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAfQAAAH0CAYAAADL1t+KAAAAAXNSR0IArs4c6QAAAAlwSFlzAAAOxAAADsQBlSsOGwAAIABJREFUeJzs3Xl4lOW5P/Dv/c6SyQJhT0ABLTHuBG1RK6Vqj8ii3UC7qdjTemol6DksAdvfqaXtOa1kAvYowXJa27pw2nrEnlYMRK2oCLXSymLrEhMFZElYs8/+3r8/kgkJZJkkM3O/78z9uS4uhQvyfAPJfOd53+d9HkAppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSSimllFJKKaWUUkoppZRSqY+kA6j088ALnOswMSLCyHKZcJsEDzPcADKo/Uek/b+GAbdpggAEGAgQIchAwNH+cwABJgRMIGCY8LsycXzRdVQv/CmqQeC1K88HGzOkcwwIGwyKNIGMRkS4HsSNMFz1cEQa6a6lx6TjqdSmha4S4oEXOJdCuJCAQgIKmHABGOcR4TwA2QkdnOFjoJoI7zPjXTJQzSaqwkDVd+fQ0YSOrQaN13pvA9MT0jkSglEP4CCAD0H8Okz6K9j9Z7r33kbpaMr+tNDVoJVv4ZzWAK4B4xoAnwRwEYARwrG6xYwmIvydgdcZeJmdeOW+GdQgnUudktKF3iN+B4ydMOh1gHbQgiWvSydS9qOFrvrNW8nZzJhOJq4F4TMApkpnGhTGThC2sIEt2W68XHwdNUtHSmfpWejdeh3MW8B4ke4peUk6jLI+LXQVk9IKvoYMzGAT1xJhmnSeRGLG60TYYhJeWD6LtkjnSTda6N1g+ED8ChiVIP4tFS+rlY6krEcLXfVo9WYuiDC+AeA2AOOl84hgHGRgvYPx6JIbqUo6Tjrg8rJbATwpncPSmLeB6H9hRv6X7ll+SDqOsgYtdNXFTzbycIcT84lxO4CPS+exFMZOAI87DDy+eBadkI6TqrTQ+4tfBOPntLDkKekkSpYWugIAeCv4syB8HcBc6Sw28XsT+PXy2fRH6SCpRi+5DxSfBLAeJpXTPUvflU6jkk8LPY2VPsf5INwD4JtEyJPOY1NHmPELMB5ediPpfc040Bl6HDBeBfM6uqfkf6SjqOTRQk9Dqyr4sgiwhAi3SmdJMU8ajNVL5tBO6SB2pjP0eOIGAD+Hk1bqxjapTws9jZQ+z1MoggcBXCudJaUxXiIHli2dSX+TjmJHOkNPAOYWgB6E6fbqJjapSws9Dax8nsdRGKU6I0+6J5yE5Ytm0WHpIHaiM/QEYpwA4T+Q1fwI/fMKv3QcFV9a6CmsfAvntPixnIB/l86Sthg+EEpbwihd8VlqlY5jBzpDTwLmAzBwPy0o+ZV0FBU/hnQAlRilFby01YcPtcyFETIBfD/biQ9LN/O/SsdRCgBAdDaYfslryv7Oa1bdJB1HxYfO0FNMaQXfDcK/EzBOOovq1kcAflAymx6VDmJVOkMXsQkR9x107716eJGNaaGniNLneQrCeKr9NDNlfbsNwh1LZtFu6SBWo4UuhHECTP9M9yzRvRVsSi+5pwDvJvZSBDu1zG2lyGTsKq3gH0gHsRxinWhIIIyAwX/gNd7f8dqfDJeOo/pPv3FszFvJV3IET2iR2xsD/4ADty27gXZJZ7ECnaFbAdeCjdto4ZI/SSdRsdMZuk15N3EpTLyuZW5/BFxMEewsreD7pbMo1YbyQfwiryl7iH+1wiOdRsVGZ+g2s2ozF0UYvyPgfOksKgEYO00Xbl0+g96RjiJFn0O3nGqYxly6Z/Fb0kFU73SGbiOlm/g+k7FLyzyFES4zwnjbu4nvlY4ihomlI6guCkDmX7h81Zelg6jeaaHbwIot7CndxE8R8BPpLCpp/stbwb+UDqEUgPb9FPi3vMb7oHQU1TO95G5x3koegwg2g3CZdBaVfMx4xQN87t45lDb7b+sld8t7DRz8Ai387nHpIKornaFb2KrNXIQI3tQyT19EuCZA+FtpBU+SzpI0esnd6j4Fcu/kR1bp65LFaKFbVNkmnhkxsR2Es6SzKHEFRHjDu4k/KR1EqXbjYZrbee2qW6SDqFO00C2otILnM7CZCFnSWZRljACw3buZPy8dJOF0YxmbIA+Yn+I13h9LJ1FttNAtprSCVxLhMekcyqIY/1e6iRdJx0goveRuL0Tf4XLvw9IxlBa6pZRu4qeIsEw6h7I2AlZ7K1hfQJWF0EIu9+pERJgWugWseJazvJv4BQL0fpSKDWGhdxP/RjqGUqfQfF7j1a9JQXqvStjqzTwibOJPRJginUWCL8jwBRmhMCMUaf8Rjv4cCIUZDMDlILgcgMtJcDkJbifB2f5rmW4DWRnp+aXMjOedw/CFxVeTTzpLvOhe7rb3f1S89IvSIdJRer4KWsSPK3i0i/AqgAuksyRSMAw0tETQEjDRGmC0Bk20Bky0+ON7qzQrg5CVYSDLTcjyGMjOMJCbZSDDldpf5szY1hrBDSs+S63SWeJBCz0l/I6Kl35FOkS6Se1XOgtbvZlHRBjbkIJlHgoDx5rDON4YwcnmCJrjXNz9leUmjBjiwMj2HylZ8IxXWzIxc8V15JeOMlha6CmC8QQtXDpfOkY6cUoHSEcPvMC54RBeJkqdMj/aGMGR+jCON0XQErDWIuXWIKP1eBgHjocBAJluwqihDozJdWJMrkM4XZwQPp3tx7MAZkhHGTRigj65Zn+E27nc20DFJfdIR0kX+l2TZA9V8FA/YQsBl0tnGayWAOOjYyEcOhFGIGStEo+VywmMG+7CWSOdyM1KgTWijGdL5tDnpGOkC169OhNufxZMRyYMZxYokgU4sgBzJBgXALgQwAUgXADQcOm8IpgW0sIl5dIx0oEWepJ5K/gVED4tnWOggmHg0MkQDh4Po7HVlI4TVzkeA2ePdGLcCKe9L8szflUyh74hHUN1xY94x4AdF8I0p4N4OkBXA8iRzpUUJmbRPUsrpWOkOhu/atmPdxP/GsAd0jkGwh9iVB8O4qNjYekoSXH2SCcKxrmRadNiZ8LyZbOoVDqH6h0/svoKmOZ0gK8B6LPSeRKHmwDzSipe/o50klRmz1crG/JW8HIQHpDO0V/+EKPmcAj7j4Wko4g4e5QTBWPtWexMuHnZLNognUPFhtc9kIuI86sw+esgulI6TwLsRYbxcbpz8QnpIKnKfq9SNrSygr9gEH4vnaM//CFGTW0I+4+mZ5Gfbnz7jN1js2JnwseXzaI3pXOo/uG1K88HO74O4HYghQ5oYrxKC5deIx0jVdnr1cmGVm/mgghjJ2xyryxiAlWHgth7RIu8O+eMduG8cW447bI4nnHQmYlLFl1H9dJR1MDww96vgei7IFwsnSVOSql46XLpEKlICz3BSiv4bSJcKJ0jFgeOh/HewSCCYXuuWE8WlwM4/6wMjB9lj6c+Gdi8bDbNls6hBofXeD8Pov8HYKp0ljiYR8VLn5EOkWq00BPIu4mfAHCbdI6+nGwx8Y/9ATT5UmvVeqJlewxcMiEDI3Ks/7ibLpJLHbymbAYIKwBcLZ1lwJhb4HBeQncv2isdJZVooSdIaQV/gwiPSufojT/EeHt/AHUNEekotjY614GLx2cg023tbycCpi+dTa9J51DxweWrvgw2y0B0tnSWAdpOxUunSYdIJdZ+BbKpVc9xYcTAbgI80ll6cqwxgp0f+hHWLo8LpwMoOsdj9Z3nPspgXHLvHGqUDqLig9ety0K46XsA7pPOMiDMy2hhiVc6Rqqw/rVCGzIJG6xc5u8cCGJHtZZ5PIUjwN9q/Hjno6B0lN6M9xN+IR1CxQ/ddVcrFS/9DsgxCcCfpPP0G1EpP1yWMltgS9NCjzPvJvaCcIl0ju74goxt7/h0BXsC7T0awrZ3fPBZdCtcAm4prWA9MCPF0IJFH1Dx0uvB+DqAZuk8/WLgf6QjpAq95B5H3gr+DMia75KPNESwe6/OypPFypfgmdEaIVz8ndmkC5JSED9UOgmGsQGEIukssTNLqHhZmXQKu9NCjxNvJWeziSoCxklnOV1NXQhVBy19KThlnT/OjY/lu6RjdOe1ktk0XTqEShwuLysDsEQ6R0wYPjgcF+mq98HRS+5xwiZ+asUy//v+gJa5oPcOBfH2fkv+/X+qdDMXS4dQiUPFS5cC5kwwH5fO0idCJiJhSz8VZAc6Q48Dq15q3/mBH7X1eo3dCvKGOXD5xyy2TpLhI8aFS2+kfdJRVOJw+eoCwHwJwHjpLH1i/jItLHlKOoZd6Qx9kFY8y1kAHpfO0VnEBF6v8mmZW0hdfQR/qfIjYqW9ewiZTNb62lXxR8WLq+F0XAmgWjpLn4hWSkewMy30QcpyYDnIOocnhMLAn9/z4WSzlZpDAcCJ5gher/IhaKUTaAmfXrmJPycdQyUW3bXoMDh4FYCd0ln6cA6v8S6WDmFXesl9EH5cwaNdhCPSOaIiZluZ6xau1jY008BV52fCYZW304yqkjl0vnQMlXjs9WYjE5Ugsu4ObYxGeIxz9ZjV/rPKS4otOQk/ls7Q2V+r/VrmNtDoM/HXar90jFMIhd5NfJd0DJV4VFLSQgtLPgXwZuksPSIMRSDyHekYdqSFPkBlFXwRAXdK54h6s8aPE816z9wuTjRHsPMDC5U68ENvJWdLh1BJ0oqbwXhDOkaPmIp5Xdko6Rh2o4U+QEywzMlVf9+nB6zYUW19BP+wziNtYzhik2eW1aBRSUkLQo6ZAL8nnaVbhEyEWGfp/aT30AdgVSVfbZrYJp0D0E1jUsEFZ7tx7hhLbD7T4iBMWDyL9N5lmuCHV44DGX8G0QTpLGdg+ODCBLpr6THpKHahM/QBiJh4WDoDABxtjGiZp4B3DwRxvMkSV1iyIya+Jx1CJQ/ds/wQyPFPYFjvTZzO0vtNZ+j9tLKCv2AQfi+dIxhmvPL3VoR1DVxKcDmA6RdlIcMl/y1pMsYvn0MHpHOo5OE1ZZ8G4RXpHGdg+JAZyaNvLm+SjmIHOkPvJwP4kXQGoO2oTi3z1BGKwDKL5Ih0lp5uaOHSV8H4vnSOMxAy4XfoFsUx0kLvh/YtXsWPRq06FER9i7Z5qjnZYqKmVv5oWwK+9VAFD5XOoZKLFi79IRivSuc4Ey+STmAXWuj982/SAazyoq8So+pQEA0WeLPmN/Bt6QxKgMvxFYBPSsfoisbwWu8/S6ewA/kbdjbx4Iv8sXAINZIZgmFg69utCIZZZPwhmYQhHsJZw6nj/0/X5Gc0+RgHTzKON5kIWGmbU5vIcBE+fVEWnLJHqX9UMtuCK59VwvFa741g2iidowvmv9DCkqukY1idFnqMSiv4p0T4V8kMuz8M4NDJ5DZkQZ6BGy51omiiAwV5/b+gU11nonJPGNurIqhtkJ952sX4UU5cMiFDNAMB85bOpmdEQygRvKbs5yDrbJzVJnIRFS9/RzqFlTmlA9hB+4lq/yKZ4XhTJKllPnOyE/Onu5GfO7j3fAV5BgpmuFE8A9hWFcYzO8LYtc8Sj2hZ2kfHwhg/yoXcLLm7YswoBqCFno5CjhK4IjeDMEw6yinGNwCUSKewMr2HHoNsB24lQpZkhrf2BZIyztypLvxhcRaW3ZQx6DI/3bRCJ1bd6sHqWz3Iz9Uvvb7s2Zucf/MeET6zejMXyIZQEmjRonoYsNYz4Iw7pCNYnb6qxkZ0MVzN4RB8wcTeN58y0YF138xE8Qw3crq5Nx5PRRMdWF+cifnT3f3+swV5BoomONLiDUGz38TeI7ILICOMu0UDKDG0YOnPwPymdI4ORKN5rfdG6RhWppfc++Ct5Cth4iKp8VsDjKrDid0Nbv50N+6YnvytR++Y7sK0Qge+/3Sgx/vrMyc7UTTBgWmFjm7faNQ2MGrqIti1z0zJ+/TvHQxi7HCn3IYzjDsB3eM9bRF9G7DQIS6MLwF4TjqGVemiuD54K/iXIIg9MrHjfT+OJWhb0BwP4YfzMlA0UXY5dbOf8f0NgY576/m5BuZOdWLmZGe/rxbs3hdB5VthVO5JneX1+cMcuOxjHskIt5fMpiclAyg5XF72KwBfl87RhpuouET3SOiBFnofSiu4kQhDJMaubzHx5/d8CfnYOR7Cqls9A1q5nijlLwRRkGdg5uTBXziqbWB4NwZSZgHepy7KxBCP2L/VcyWz6SapwZUsfuTBc2BGPpTO0YHps7RwibUeq7MI67yaW5B3M39eqswBoDpBl9qtWOYAUDzDHZcyB4D83LbP8Yc3ZyR8TUAyVB8SvZd+48rXWOz7QMmiuxftBdg6V2jIvEU6glXpPfReMOPLUlXQ7DNxtDH+s8t4lHldA6O2wURtPaPutHvWk/IM5OcamGSRNwvTCp1Yv8DR5ZJ+ZwV5bVnzullkV1NnotnP2L1ffpZfWx+GL+hGplvmK5IacQuAX4oMruQZWAkTt0nHAAAwfU46glXZf+qSIKu3c2akHsdByJQYf+cHftTWx79IVt/qGdA987oGxraqtnvT1XV9LzzLzzVQNNGBeVOdlin30o1BbKsKY1ph2yK7ogndL7TrTnWdiW1VEWyviu3zT4SzRzpx6USxzWYqS2bTLKnBlTwu9/4RoM9K5wAAEBfRgpI90jGsRgu9B95N/EUIbarREmC8+o/WuH/cO6a7+v2oWF0D47GtIVTuGfgl3ykTHZg/3YWiCbKL7+KltoGx4Y0Qnn8rjGZ/crfhve7SLHiEVrxHnBh23wxqEBlcieOHV34ChmOHdA4AAPMSWliyWjqG1Vhj6mRNM6UGrknAvfO2Uu1fmT++NYivlbcOqswBYNe+CBY/6cfaF4NoCcjsQx9P+bmE4hlurF/Q9ix9Mu/Rfyh4MI8jjM+IDa7E0T3L/wrmbdI5AACEGdIRrEgLvQfMENnAIBhmHDwR/0eu7r4+9jJvCTCWrPfjsa3xLY8Nb4Sw+Ek/6hrsX+pA23qEO6a7sH5BZtwW8/Vl/7EQwnKP2ou9yVUWQXhMOkK7T0sHsCK95N6NlZv4fAN4V2LsvUdCeOdAfGfo865wYUGMhV5TZ6J0YyCh94lzPITVt3piurcevXe/a5+JugazI9eU9nUAk/IMzJvqQl6ct6kdiN37Irh/QyDhl+EvnZiBs0cmfz0rM/Yvm0MTkz6wsgxe+5PhYNcJ6RwAAMO4ku5ebJ1NbyxA/lXQgryb+F4A/yUx9qtvt6IljoWQ4yGsX5AZ02XhlgDjW7/wJ2W3tb5Kfff+CB7fGor5OfKCPAMLZrjF79OfvklOIozIceDKQpmNZtiBwmU30PsigytL4DXeZ0D0RekcABZT8dIHpUNYiV5y794NEoM2+cy4ljnQ9thWrPd4Fz+ZnDIH2orv/qcDZ9xTbwkwSjcGsfhJf79KsbrOxOIn/d1+zGSKPhY4c3LittI90RyBPyTzORom/klkYGUdZJldAz8lHcBqtNC7d43EoAeOx//e+fwY92hf+2Iw6Y9j1Ta0lXC0gHfvj+Br5b5BLcLbVhXG18p9qBF6tCxq2U3uhJb6oQR8rcTCZL13me6oeOkzADdJ54DeRz+DFvppSp/nKQByJMY+eCK+i9AK8oyYjkCta38MS0J1nYmVzwax9sW2WXk87j83+xmL1/tjLvWaOhO790e6/IjHwr1Elvr+Y2Kr3UXe7CqroQ3SCQCM4vJV46VDWInuFHcaisi86zvaGEEozpOuuVNjK5N4r2bvr21V8Z9tRkv9f4ozkZ3R9U1NdKHdtqpIn5f1p0x0tG9E4xzQwrtlN7lRUxeJ+9UPX5DR0GoiNyu578kJGOet5HNLZpJ19vZWyUf8JzBZ4MCWyMUAPpJOYRU6Qz8NC11SrK2Pf6nFsiNcTZ056OfMrarZz10u6W+rCmPJej++Vt6K8heCMd2j37UvgvIX2p7HX7LeP6BtYH9wsychz6rXJeBrJhZk6qXOtBcxX5KO0O4S6QBWooV+GiJcITHu8Tjv256fG9vl9sq3UueY0e5U15m4/+kAbi334f6nB7f6PLpBTunGYL8uyefnEpbd1L9NfWJxPEHH6vaFGZ8QGVhZBt2z/BCAD6RzgA0t9E600DtZ8SxnAUj6PRlfiOELxnfVcqz7tW97T/7gkUTbtS8S19X7lXtC+Naj/Vt4N63QiWmF8b3DVd9iIizwz8eEi5M/qrIcxsvSEQDWr8VOtNA7GeLGFIlx4z07B4D83L5/T02dmbTH1FJNs5/xrUd9qNwT+xWOBTPiv03syWaRN2STJQZVlvOqdACAPiadwEq00DuJmDL3Y44loNBj2YXNCseC2l3pxkDMpZ6fS5g3Nb6z9ER87fSFgJE/ruDRSR9YWQuzfKETRvC6dVnSMaxCC70rkUJPxL3QWGaCyT4pLFWVbgzEfPl97lRXXGfpx2Vm6HAYuhgp3dE9JdZ40iHYNEE6glVooXdCwIXJHrPZbyIYlinW5oDIsClp8frYDp3J8VBc76U3+UwEBdY1kokLkj+qsqC/SQcAJX/dk1VpoXfCjKTfj6lvScw97Lzcvv9pE72bWkGekbS91fNj+HwTqdnPMT/PPzfOl90bWwUuuxPOTfqgyoqqpAOAWGfo7bTQOyFKfqG3+BNTqnUWWOy2YIYbq2/zdJyMlgjzp7vxp+9mY31xJv703eyEjROLyj2hmN4kte3gF79vvZaAwL81a6ErAGD5Qgfpeo52WujtvJUs8gLVnKBCj0XRBHv/88+7woU7prtQ18B4fGsQj2+N77GzA7H2xdgyTDs/fm9ymn0Ct2x0hq4AAPSedAKAR0onsArd+jUqgnMlDpNN1Ay9tp5RlOIXoqJb237rUZ9lFvjt2te2D3xf28QWTTCwIU4nOYvM0KGFrgAQqiD9rcc0QjiBZdh7ihZHTBCpv0Qd9VlzpO8X+Vg3n7Gi6MEzu/dHLFPmUbHsTR/PtQVCV3lGtG/EpNKZw3FIOgJIZ+hROkOPYoxK9gw9ked2x3Ivt7dSaVuN7ehYXLd7X+SM59anFTo7nndv9jO2V8W2I1tBnoGr21d61zWY2FZ1Zimf/nt27zu1Cc7cqS4UtI+bl2tg/nQ36hq4Y0/6zrlq6swuBZufa+CGyU7saX8jEB3j+T1h1DaYyPEQiiY4evy8CvIMTJ7gQI6H0OxnPP9W+Izsu/aZmDu197+DHA8hwwkE4rBCPSB0NvoQN0YCaBUZXFlDY7gRWQKXNrvSGXo7LfR2BIxK9piJutwOIObTvaZMdJyxv3lBnoFVt552oMh0F2rqTHzrUR8A4H+Ks864rFw8A3h8a7DH1d45nrY9zU9/bKvZz1iy3t+RedlNGZg5+cwvzfufDmD3/giKZ5zaFz0/l3DHdBcq94SxrYqw6lZPR9lHVde58P2nA6htMJE/rO33V9c5uvy+Z3aEUJBn4Ac3e87YA58oiA1vmFhwvRvzruh6gt0d011dsgPRGXpGt38HnbldhECcHlmUOHktQhgJPekqrVFJSQuXl0mnEDnu2oq00KMo+YXuCyau0GM9DGRa4ZmFPn962+YnpRuDqNwT6vbZ6Q07Qqit545L3lMmOvDDmzMwf7oblXu6n6nfMd2FaYVO1LQfmFLbYGLeFS4suN6NBde7sXi9HwV5BmZOdmL3/gjufzqAZj93+bVo+S+43o1JeQbWvhhs28K2nvHDeRkoyDNQuSeMx9vfVMyf7sLMyU4su6nt40cV5BnYVhXGMztOzbCjb2Ke2RFC5Z4wqutMFOQZqG1gzJzswrwrXN1mX3WrB59f3XWi2hLgM45tPV2WG2jyxfTP1CdfkJGb5AvgHIFe6lQA+CRAwwXH10Jvp4V+StILPZygPu/PQSDdXXaPzsyjM/BmP59xxOqGN079vGiCA7X1jNfei2DmZCfyhxFqG84c64ZL2zJFCzH6cWZe6kTRRAfyc41OYxvIyWi7rF1dZ6L6hVOrx3fti3Ssw6ncE+4o/aKJDrQEGKUbT+2YU7oxgCkTHSia2HVGXtfAuP/pU79v3hVtb2J27287LjUqOvOOPjv+2NZQl+xFEwxMK3SecaWjus7s8z65wyAgTiuKwpHkX3Y3SAtdAWBqBEGw0HWGHqWF3o4ZwyjJt4IiCXgRjl7WjsXp5Re14Y0wiiY4cMd0F+ZNdWJbVQTPvxXuUljTCp2YP911xuXtnhTknSrr0/NF3zjkDyPs2hdBTZ2JSXkG1hdnorrOROWe8Bn3qgvyDLQEuOPXovf6u7vVUNtgIi/XgUl5jo7n80+/ghC9zL67h+NVo5/nvKnOLvux5w1r+/VJecagjmYdLIndBomT/yZYWVKj7PA6Q4/SQm9HlPyHL8wEzNDvmB7bXuEtAcbiJ/3dFuC2qjBuLTcxf7oLUyY6MHOyEzMnO1G5J4zSjQHk5xr44c0ZaAlwxyVvoO3ydk+z0s6ZTl9cF/15bX3bP8G3HvVh5mQXZk52oGiCAwUz3F3uVUc3qumcPd6nmPXkjANt2n8ufQxtSKDQTV2MpAAA3AyJZ3470BDBwS1FC70dM0JJn6HHudBzPNRxWbsv5S+Eel04V9tgdszeo/fHZ0524vGtIcyc3FaoG94InXbpveetXjvPXjfsOHNl+Okq94Q67t8vuN6NmZOdmDvVhdKNgY7ZeOeV/NGZd3db3kZ/rbfd82obus70Txd9try6jmN6LC3ZJAodWuiqjfy2lAqAPofegYCkv0pHzPi+CM+b6oxpplq5J3zGPfHO7mhfSBa1a18ETf4zf18sR7SePi5pwkjvAAAgAElEQVQA/HBeRpecOR7q2Aq1IK/tMbToz5v9jN37T7883vbf6rpTf3/RDV3yc6nLSvSZk13IzyXUNXCvl8Qr94TREuCONw6ds+V4qOPva/50V5dtWztn7yyWvfTjKSRwgYC00JWyFJ2ht2NCKNkXjeLc512KqCfRy+S9mXeFC9kZhGU3ZWD3vggmtd//rmx/VrtyDzDvCsa0QifWFztQV28i20N93k9f+2KwY/HaHxZ3XZK9rSqM+58OoGhi2737O6a7UNvAHQveWgKMZ3a0lWp0Q5zTZ9z3P+3H6ts8WHC9G/M/1fZ3keMhtAQY9z/dzTuSTpr9jPIXQlh2kxvFM9xdHo2LPoo3Kc9o/5wzu/zZ2gbGreVdV7mf/uhbd5riuCFOSGBRHFgLXSkr0UKPYoSSfRsonovipkx0xDQ7L38h1Ofl7s+tasW0QicK8ghFEx14/q0wqutOrXSvbTDxtXIfZk52omhCW9nX1JnYXtX2+6KX8qOXxKP3xpv93HF/vCCPOmb4u/dFsK2qbYq54Y0Qtr0XwbTzHZg0xkCOB9heFe7yKNykMW1/7vQZd3Vd11wAsHu/2bESPpph9/5It4vfKveEsHtfBDMnO7psTBO9QnD/0wFMmRhuu7Uw0YFmP6OmzuxypQBAzAsFg3HcEEZilTvrDF0pS9FCb0dA0k8Hdzji9w5iWmHfW4l23k2tL9uqwthWBaCHTWKa/dx+D73nj9H58a/OKveEUNnL2LUNJja80f1tueijbT3thNdXruo6E4uf7Hm2Xttg4rGtPd8S3LUv0vZGopejUrvbFKc78dglLirZ6z+UUtaj99DbMSHpR3U54vi3PzmGvcGtuJirv6KnlJ2x2txCro5hD4B453caAo0u8D2jlOqZztBPSfqLUzxfhGO5zLtrnz0Xo+Z4qGN9QPQZ8A1vWPPNyZSJjpjun/f0vPtAOWXO2Un6VS2lVM+00NsRI5jse+iOOL0IZ/WxxWiUXWfo0wqduGP6qQV/pRuDMR0CIyG6GK8v0TUD8RLP2zexkrhNpZTqmRZ6lMDlQ1cSX4QTebJbom2rCmPJ+rYCr64zLXdcalR0i9m+1DVwzIfnxMolccldC10pS9FCP6Up2QPGa1bljmGmH+8CSaZmf+/PkFtBjodw9/Wxbbm7YUdsCxP7I15Xe/op6d8zSqme6aK4dsw4nuwx43Xf061vy8QtuN4d0zqGlgB3bLATT06BS+5gHEv+oEqpnmihtyMj+YXulngRVnF3+s56vdnwRt/7AAxEhjP5X0sMLXSlrEQLvR0JzNCzPfH56w/GMOFL9lak6WLuVBfmT4/9dLsNOxKzMDErTl9L/UJa6EpZiV6sbRcxcdxI8mtipjs+s6pgDLeXY3mUSvXPspsyYp6ZA21nqSdqQd8QiUI3tNCVshKdtrVzOlEnMe6QzMH/E8R6DGusW5Kq3hXkGVj3zcx+lXlNndnlZLp4cjtJ5Dl0w5T5nlFKdU9f4dstmUkfSYybHeMz5L3xx7gneCzbw6qe5ecaWHZTBtZ9M7Nfb47aDodJ3BNe2Uk6C/4MHnwoM7BSqjt6yb0TZtQQYVIyx2y7jz74R7J274/0eBZ51NWFTjzWyx7k6SQ/14hpc5r8XANFEw1MK3RgWgxbunZn5bOJ3QgnO0PmffnS60gvuStlIVronRDhQ0Ci0Adv976+C70gz8CUiQ7LP9OdaDkewrpvepDjoY4T02obGLUNbVc68nMJ+bkU05GwfSndGEz4Dn05cbhtMwC7JQZVSvVMC70zxofJ3v41XouZtlVFMH96379v/qdcaV/oC653dxw1m+NpOyK2KAHjVO4Jx3y63WDkCCyIY9bL7UpZjd5D74QNVCd7zKFZRlxOXauuM3s8UrSzookOzJwc237jqWjKREe/FrMN1NoXgyjdmJydUUfkJH9tBBHeT/qgSqleaaF3QsA/JMYdHqcX5Mq3Yru0u+B6V1queM/xEH4wLyOhY7QEGKUbgwlb0X663Di9IewvZvw9+aMqpXqTfq/qvQizTKGPHBKnQt8TjukQlhwPoeSmjI7Lzukgx0NYdasnoZ9zTZ2JxU/6k3KZPUpidg4AMLTQlbIaLfROvjOb9kqMOyJOhd7s55hnhgV5Blbd6kF+GuwgFy3zRF6VeHxrEIvX+5N+CM7IoTKFvmwWvSkysFKqR6n/at5PDLyR7DGHxfGy6WNbQ6hriO259LYNUhJbdNKib1wS9TlW7gnjrkd9Cd0FrjcSM3RmvX+ulBXpKvcz7QFwRbIHHZ7jwLHG+Kw+L90YwKpbPTH93rZHuDJRuSeMtS8GLXvWeH/leAhzp7pwx/T4LwBsCTBeey+Cx7eGEvp8eV+k7p+j7XtEKWUxWuhn2gbgzmQPOmpI/Ap9174IntkRwtypsZfZzMlOTCt0oHJPGM+/Fbbt+en5uQZumOzEvKnOuN4vbwm0ncm+rcrEtqqwJd74xGvtRb8Z2CozsOoPLi/7Kph/DqJs6SyJxuVlSfiG5P+k4pJ/T/w4A5c+q6JiVFrBk4iS//iaP8TY8lZrXD/mf38zE5MGeKm5toGx7b0wmgNAXYOJ2npGjoc6Pt72quSXfrSsgVOZAGBSnoH83LbnyQd6af2ZHaEuf1c1dSaa/YzqOkZdg2nJNzjTLszEUIFNZQzG5Uvm0M6kD6xixmtKLwcZf5POkXIYd9HCpf8tHaMnOkM/zbI5VFO6iQ8RMC6Z43pchBHZBk60xK84Fq/3Y/WtngGVen4uYd4VPc/wZ0524q5HfUmdqS67yY2iifGflZZuDCZ1ZXo8ZHtIpMwBNGuZ24HxeekEKepmAJYt9NRdDTUYLHNJcdzI+N7vbfYzSjcGYtpwpr/ycykh96d7Mu8Kl5Z5J+NHiW0O9IrUwKofSE/CSxCRQ7xipYXeDSJskRh37PD4XzCprjOxeL0/IaU+d6oLUxJQsqcryDMw/1PxLbDoBjB2LHMAOGuEzMU1k2W+N1Q/OYf8GoDIY7gpi+GDESmVjtEbLfRuRJzYJDGu0wHkD4v/C3Wzn7F4vT8hh4T8YF5GQh97S8QmOHUNnPQNYOJp1BAH3E6Z5S/MeF5kYNUvdNddrTAc14H5gHSWlME8hxYsf086Rm90UVwPvJv4fQAFyR73aEMEf63xJ+zjz7ui7VGueJzDHtXsZyxJwKYqidgQZltVGKUb7f143pRzMjBWYIbOjKPL5tCYpA+sBowfefAcRMJbQXS2dBZbM/k6uqfkZekYfdEZes9EZiKjcx3IcCXufdaGN0L41i/8qNwTv9l6tHjjefm9bdObzLiVeV0D4/6nA7j/6YCty9zpAPIScBUnFgRsFBlYDRjdvWgvHM7pOlMfBJuUOaCF3iMTqJQa+2N5iV3wVNtgonRjALeW++JW7NFS73w06UDNn+7Gum9mIj938G9s6hoYa18M4luP+hJ+LnkynJvnhiH0XcuC3xNq4LTUB8FGZQ7oJfcelW/hnFY/mqTGf3F3C0JJOrY8x0OYOdmJmZc6B/zcemfNfsaGHWE8syP27VBzPIRphQ7Mn+4edJFHd3LbVhVJiRKPchrAdZdmwym0n4zTg+GLrqN6mdHVYOnl936yWZkDWui98m7iDQDmSoy990gI7xwIJn3cHA+haIIDBXltm8hEZ9sFecaA7rtvqwqjuo6xe18ELQHuuM+en2sgL7dtjCkTDUwr7P9l5M4fr7aeUXOk7Uz4XfuS9E4oyQrHujFprNjjas+VzKabpAZX8aGlHiMbljmghd4r72b+Ehi/kxg7wsCWPcmbpfelIM/A6ts8cV1MN1j3Px1IqRl4b6Rn5wBuL5lNT4qNruJGS70PNi1zQO+h98oxFM+C4RMZm4BJY90SQ3eruv2s71jOW0+G0o3BtClzoO3euWCZwxyCP8iNruJJ76n3wsZlDmih92rx1eQD4Vmp8SeMcsFloc15rVLqdt4QZiCcBnBOghdK9uGZ5Z8isfUkKv601Lth8zIHtND7xAaekBrbYQDnj8uQGr5b0VKP9cz1eGoJMO561JdWZQ4AhWe54RT8TjVZ7ntAJY6WeicpUOaA3kOPSWkFHyHCaKnxX3vHhyaftU77yvEQlt3kHtBitoHYvT9i+2fIByLbQ/j0RVlyARjHSuaQ2Ne+Sry0v6eeImUO6Aw9NoRHJYe/ZKK1ZulA26Np9z8dQOnGYEIvwbcEGI9vDWLxk/60K3MAuHSiR3R8Bn4pGkAlXFrP1FOozAEt9JiQIXtc3rAsQ+wwjr5U7gnha+U+PL41/sVeuSeMr5X78NjW9LrEHjV2uBPDs2W/RR0s+2ZWJUdalnqKlTmgl9xjVrqJXyVgutT4wTDj5b+3ImKtK+9d5HgI86Y6MXOyC3kD3BymroFRuSeEyj0R1DZY+JNNMIOAay7JgieB2wD3hYGty2bTp8UCqKRLm8vvKVjmgBZ6zMo28VwGNkhmkNpsZiDycw1MO9+BogkGCvIcPRZ8XQOjtsHE7n1tO7vF+4AXuzr/LHfCtwDuCwHzls6mZ0RDqKRL+VJP0TIHtND7xbuJPwBwrmSGP7/nQ32LfUvP0X4F2cpXGqTlZhm4+oJM0QwM7F02m0S/1pWclC31FC5zQO+h9wszvNIZPj7JI3YWdjxETC3z3rgcbf/G0gh4QDqDkpOS99RTvMwBLfR+cQ7Dr5lxUjKD20m43AIv+CoxLp+UmdDjc2PBjJMls2mdaAglLqVKPQ3KHNBC75fFV5OPgFXSOYZnG7jgbOtsC6vi4/yz3BiRI/8tScBK6QzKGlKi1NOkzAEt9P5z4KcATkjHOHeMC2OGCm7ureJqdK5DfBFcuyMtmfgv6RDKOmxd6mlU5oAWer+VzKQWJtwvnQMAis71IMtCp5+pgcnKIEw5xxq3UZjw/1ZcR37pHMpabFnqaVbmgK5yHzArrHgHAH+Isf1dHwKh9NtFLRVkuAhXX5Ap+rx5B0ZVyRw6XzqGsi7brH5PwzIHdIY+cIR/l44AAB4X4crzMkUP71AD4zSAKwstUuYAQLhPOoKyNlvM1NO0zAGdoQ+Kt4LfAuES6RwA0NBi4s9VPrBO1G2BCLjq/EwMy7LGOzFmvL5sDn1SOoeyB8vO1NO4zAGdoQ+KaeBe6QxRudmGJZ5fVrH5xCSPZcocABzAAukMyj4sOVNP8zIHtNAHZfks2gLgOekcUaOHOnCpBU9mU11dOjEDoyz0hAID/7tkDu2UzqHsxVKlrmUOQAt90AwTi6UzdHb2SCeKztVSt6rLzs3A2SOtdXKeYaJEOoOyJ0uUupZ5By30QVpyI1Uxy28209m44U5MLfB07Juu5BnUtgAuf7i1yhzAD5beSPukQyj7Ei11LfMudFFcHKzezpmRBuwBUCCdpbOGVhM7qn0IhaWTpDeXA7iiMBNDMy33Dmt3yWyaIh1CpYakL5TTMj+D5V5h7Gjx1eQzCbdK5zhdbpaBT54ve6Z2ust0Ea6+IMuKZQ7Tia9KZ1CpI6kzdS3zblnvVcamls+iNwCUSec4XXYG4ZMXWHJ2mPJyswxcfWGmJXfzY+B7y2fQO9I5VGpJSqlrmffIeq80Nle6id8lwJK7bb39URD7joakY6SFc0a7cOF4ix6gw/hLyRy6SjqGSl0Ju/yuZd4rnbbFmWniFukMPblovBsfn+SB0zpPTKUcpwOYWuCxbJkzo8lwWPdrVKWGhMzUtcz7pDP0BPBW8EIQHpbO0RNfiPFmtR+NPlM6SkoZmmng4wUeS69ZYMLNy2bRBukcVsAPPTQURuBCGDQCJg8BjBzAzAEoB8RZYBoKwhAAOQDnAJQBcDNAzZ3+2whGC8DNMKgJoGZEuBEO8yAtWP6e9OcoLW4zdS3zmFj3lcfmSiu4kgg3SOfozTsfBbFXL8HHxbljXHY4o/6Jktk0XzpEMvHq1ZnICJ8PpkIQzgNQCG7/L9HIJESoBvA+gHfBVANwFYAqWrg0bR4VHHSpa5nHTAs9QX78Io90BvEPIuRJZ+lNQ4uJPfv8aPbrJvADMSTTwOSJGRhqoW1ce1DdEkbRis9Sq3SQROKHS6fBoGvBNB3giy2313gXvAugXWC8DDPyJ7p3ufyOawky4FLXMu8XLfQEKq3gaUR4TTpHLD48EsL7h4KI6FX4mDgdQOE4NyaOdklH6RMzWtmFT6TaqnZescKJkVlXwqBrAVwL4GqAsqRzDUI1GC+DeQvYfDXVCr7fpa5l3m9a6Anm3cSLAWvtJNcTf4jx9v4A6hoi0lEsbexwJy48240MC98r74wYtyydQ09L5xgsXrHCwMjMy0HGdSC6DsB0ADnSuRKH3wHTSyC8hIh7K91771HpRIMVc6lrmQ+IPV6RbM67if8PwOelc8TqSEME7x4IoCWgl+E7G5Jp4IKz3JY6WCUG60pm07elQwwGrysbhQi+CpPng+gT0nlEMLeAsAFsPI5jTVtoxQrbXkvj8lXjAX4J3e6sya0gxxxasPiVpAdLAVroSeCt5GyOYAcRLpTO0h9HGyP4oDaEE83pPWMfNdSBSfkujMixVZHb+oxz/tUKD1qyPwfQ7QDPApHlNsEXw3wIoPUA/YIWLqmSjjMQ/OjKIQgYC2HSdSB2A2SC8VcQPUzFSz6SzmdXWuhJsrKCzyZgBxHypbP0V0OriZrDwbS7FD92uBMFY13I8Vh+wVt3qsMRXPGdm+ikdJD+4IdXfgLk+DqAr4IwQjqP5THeAMxfw+P8Hd25+IR0HCVLCz2JvJt4Mhivg5ApnWUgWgKMfXUhHDwRQti2F/x653QAZ49w4dx8l6WfJ+8NM04ajMvscooal5fmA8Z8MO4A4SLpPLbEHATRH0H8a4yauJm+9KX0evetAGihJ513M38ejP+TzjFYtfURHDwWwpHG1HjdyB/mwFkjXRiTa6/L6mdg+EzgM8vn0OvSUfrCD68cBzLuBeFbAA2XzpNCXgfzgxgzcYMWe3rRQhdQtplvZ8bj0jniIRgGDp0M4eCxsO12nhuWbeDskS6MHe5Mne1wGf9UModeko7RG1676iowLwTwJQDWf+7Prhj7AH4IZsYv6N57G6XjqMTTQhfireB/AeG/pXPEU2uAcbQpjKP1EZxojljumXanAxg5xIExuU6MGuqw7SX1njBh9rJZtFk6R0/adm2LfAfAEps/L24vzH+B4ViuK8dTX2q9otmM1fd8H6xjjREcbYjgWFNYbCe6oZkGRg11YHSuEyNybLm4LSYm8Pnls+mP0jm6w8yEtd7bwfSf1t65LcUx/x6GcyktWPSBdBSVGFrowko3878S46fSORItbAItfhOtQUZrwESr30RrgOELmPCFBlf2mW5CVoaBrAxCtsdo+//2X3Okbod3sPLGMbzG+0WAfgTCxdJZFADmMEC/hstxP9216LB0HBVfWugWkIqX3/srFAaCEUY4wgiFGSGTEQoDoUhb2bsdBKcTcBkEl5PgckT/KxxcGuGmkln0nHSM0/HD3mth0E8A6LnrVsTwAVgDF0rprqXHpOOo+NBCtwgtddVvFixzXlc2CmH8HMAXpLOoGDDqQbSIipf8WjqKGjwtdAsp3cx3EuPn0jmUtTGj1SDMXTqbKqWzdMZrvF8B0cMARklnUf22CWbkTrpn+SHpIGrgtNAtxlvBnwGwAYRh0lmU9TDjgGlg1n2z6B/SWaJ43YNjEQ7/GqAbpLOoQdDZuu1poVtQ2XM80TRQScD50lmUdTCwNezCF797PR2XzhLF5WU3g/FzfQOaSvhZGI676e7FB6WTqP7RQreo8i2c0+rD/4DwWeksygIYPy2ZQ4ukY0Txgw8OgzvycwA3S2dRCcCoB/huWljyW+koKnZa6Bbn3cz/Acb/k86h5JiM25bPofXSOaJ4bdlsmPwLEI2TzqISjPm3CDnvpkWL6qWjqL5podtA6Sa+hYCnpHOo5GLGSYcDNy2ZSduls0Tx2rJvg7EGQLo/MJhOdsJwzKW7F+2VDqJ6p4VuE2WbeKoJbCJgpHQWlRTvhoHZ35lNlngR5aeecuDo/jUAvi2dRQlgPg4yPkfFSyzz5lKdSQvdRkqf43wY+BUBs6SzqIRa58jFosVXk086CADwQw8NhSOwAaDrpbMoQW1HtH6Dipda5vaP6koL3YbaN6FZDSBHOouKH2bUEeErJbPpZeksUfzI6rMQMZ/Xc8pVB8YPaeHS70vHUGfSQrcpbyWfyyYeI2C6dBYVF086Pbhn0XVkmcVHvLbs42D8AcBZ0lmUxTB+iTETvqXnrVuLFrrNlVbwPUT4CYBs6SxqQI4w4/Zlc+h56SCd8cNlM2HwM3rMqerFJjjDX6W77muQDqLaaKGngJ9s4nMcjCeJME06i+qXxyJO/Ot9M8hSL4i8dtUtYP4NdCW76gvjLTj4erq75Ih0FKWFnlLKNvO32cRKEIZKZ1G9+pCAu622FzsA8Brvv4FoNfS1QcWuGjBmU/Hiaukg6U6/aVPM6s08ImziP4hwt3QWdYZmBv5z2Wx6QDrI6ZiZUF62GkT/Jp1FQiQQQKilBZGAH2YohEgwCDMUQCQY6vg5mxEYThccbjcMlwuOjIz2n7tguDPgzMyCe8gQ6U9FCB+B6bie7ln8lnSSdKaFnqIe2MwXGybW6WV4y3gMBpaVzCTLXZpsf8b8NwBukc6SSByJwH/iOILNzQg1NyHU0oJwawuCzc3gSDhu4zg9HrhyhsCVlQ1XTg5c2dlwDx0K99AU3+6+7XCXuVS8ZIt0lHSlhZ7iyip4NhN+BODj0lnS1B8iJr53341k2ZkLryl7FIRvSOeINw5H4Dt+FL5jR+E7dgT+EydE8zjcHmSOHoXMUaOROXoM3ENS8M4Y4wQM3EALlv5NOko60kJPEys38ecM4IcAiqSzpInnDMb3lsyhndJBesNrvA+m0mX2QP1JNB88gNYjdQjUn5SO0yvD7UbmqNHIzsvHkLPHg5wu6UjxwTgBinyKipe/Ix0l3Wihp5mVFfwFIizW59cT5rdkoGzpTLL8DIXXeB8A0XLpHIMVCfjRuH8fmvbvRbCxUTrOgJDhQM64cRgy8RxkjcmXjhMPh4HIP2mpJ5cWeppaVcGXmYRFAG6XzpICTjDw3+zAw8tvoEPSYWLRvpr9QekcA8WRCJoPHUTT/r1oPVInHSeuHB4Phpw9AbnnfgyuHBsvsmM+ABddRnctPSYdJV1ooae59v3h7wTj60SYJJ3HZl5jxq+cw/Abq+y7Hgte670eJipBZEhn6S8OR1D/wfs4WfUuzFBIOk7CZY0ZgxEXXgLPCJueycT8ZwQd/0SLF9vm+8POtNBVh1WVfLUZwdcBfFmfZe8BYx8DjxmMXy69kfZJx+kvfnj1pSDzNbv9+3YU+fvvwQwGpeMkXdaYPIy8+FJkDBsuHaX/mDfgWMuXaMUKUzpKqtNCHwT+1QoPWrMWAsZyAKPaf/k3YFpBC5dUSWYbjBVb2JPlxxcBzNeT3QAwGhl4mghPWOnglP7iR1afBdP8C2y0NztHIqj/oBr1Ve8ikoZFfrqs/HyMvPASOxb7f1Hx0pRZfGlVWugDxGvLPg6TnwHRhO5/A/6DFi79XpJjxV3pc5wPwm0g3ELAFdJ5kobhY8IWIjzWkoE/rriO/NKRBoNXrDAwKudPIFwrnSVWDR/U4MS7/0AkEJCOYjnZY8dh1KVFcGXb6MBF5i/QwpI/SMdIZVroA8DlpVPAxit9XrZkfoQWlixIUqyEe+AFznVEcC0YnwHjMyBcIp0pnpjxCoCXYGDLslm0VTpPPNlpRbvv2FEc3fUmgk32XLGeTMMKCjHyootBDqd0lL4x6uFwXEZ3L9orHSVVaaH3U8xl3vEHUqvUO/txBY92Eq4l4FpmXEeEC6Uz9QcDW4nxMoCXWzKx3e6z8J5wufezAP1ROkdfQi3NOPbWbrQctsWDApbhcHsw8uJLMPScc6WjxGIHnEOm0V13pf6KRgFa6P3Q7zLv+IOpW+qdeSt5DBhTGbiYTBQwUEiEQgBjJXMx430iVAF4hwg1ILxtDMEOO61MHyheUzYRwC4QLLvvKEciOPHOP3Dy/feko9iaOzcXY6Z83AYr4nkdFZd8WzpFKtJCj9GAy7zjA6RHqXdn9XbODJ3ExUSYBMJ5YJxHhI8xYxwBY0HIHOQQJ8CoZeAAEarBeJ8NvAsDNctuoPfj8knYUNt98+ztILpSOktPQk1NOPT6awg1N0tHSRkjL7wEwy+w+MUyoi/RgiX/Kx0j1Wihx2DQZd7xgdK31HvzUAUP9RHGEmEMcYxncBvwRQwcvm8G7U9wPNvicu8KgL4vnaMnjfv34uiuv4Ej+jRTvGWOHoP8qVfBkZEhHaUHfBJO58V016LD0klSiRZ6H+JW5h0fUEtdJR6v8V4JYLsVN4/hcAR1b76B5oMHpKOkNEdGBvKv+CQyR42WjtIDfh5HW2br8+nxY7lvdiuJe5kDANHdvMa7Nm4fT6nT8NqfDAfwGyuWeaipCfv/VKllngSRQAAHt76Mk+9adTt1ugGjc5ZJp0gllvuGt4qElHmUlrpKJHb+BESWW/LsO1KH/VueR6i1RTpKWjn+zt9x+C/bpWN0j/kHXL66QDpGqtBL7t1IaJl3GUgvv6v44rVls8GokM5xuuaDB1D7xp+lY6Q1z4iRGHf1p2G4LPfM+msYPeFa+tKXItJB7E5n6KdJWpkDOlNXccVebzZM/oV0jtM1fFijZW4B/hPHceDVlxAJWG67hU/h6P4S6RCpQAu9k6SWeZSWuoqXLKwC0TjpGJ0de2s3ju56UzqGahdsbMBHL7+EcEurdJSumH/A5aVTpGPYnRZ6O5Eyj9JSV4PEPyu7CKA7pXN0VvfXv6C+2rZnFKWscGsLPnr5BQQb6qWjnELkBmiFdAy700KHcJlHaamrwYjwj4EYn+FPgtodr6PpI90iwKoiwSAObH0ZoRYrbehDn+fyVVdLp7CztC90S5R5lBk79zAAACAASURBVJa6GgBeu+oqgD4vnSPq+NtvofnAR9IxVB/MUAgHt75ssXvq7JVOYGdpXeiWKvMoLXXVX8wPSkeIavigBiffe1c6hopR2OfDwddegRkKS0eJuprXeL8iHcKu0rbQLVnmUVrqKkbtL35XSecAgOZDB3F0ty6As5tgYyMO/dlSpwX/mJ96yjK3j+wkLQvd0mUepaWu+sBPPeUA0U+kcwCA79gR1Fp18xLVJ//xYzj8523SMdoQnYtj+/9FOoYdpV2h26LMo7TUVW/aXvTOkY4RbmnFIauUgRqwltpDOPHu29Ix2phYwb9a4ZGOYTdpVei2KvMoLXXVDf7VCg+YfyCdAwAOvf4aOJyYe7CZky9D5uTL4Mofm5CPr7o68c4/4D9+TDoGQMhDa86/Scewm7TZ+tWWZd6ZbhOrOuHysvsAiF9uP/bW7kE9a27kDEHm5MuQMakQ7knnwZEzBJlFl/f6Z8zmJgRq3keo7jD8u99EoOZ9BGr0efd4cWRkYOKMWTBcbuEk3ABnZCLddV+DcBDbSItCt32ZR2mpKwC8YoUTo7L3Se8K5zt6BAdfe6Xffy5jUiGyr/40sqd9GhmTCuOSxWxuQvP2V9Gy7RW0bH81Lh8znWXl5WPc1dOlYwDAd6h46QPSIewi5Qs9Zco8Sks97fEa71dA9BvJDJGAH/te2AwzFIr5zwy94Ubkzv1y3Eq8J2ZzE+qf+R3qf/87mM1NCR0rlY26tAjDChL7bxWDgzjafA6tWGGZ5+qsLKULPeXKPEpLPW0xM6G87A0QfUIyx8GtW+A7Ftu9ViNnCM554hkYOUMSnOpMjc8/h5NP/AKh2sNJHzsVjP/MDGTkDpMNwfxVWljyW9kQ9pCyi+JStswBXSiXztZ6Z0qXecMHNTGXOdA2Yz64tBimwDajQ2+4EeMfeRwjbr9T5A2F3dX99Q3pCADRYmZO6clnvKRkoad0mUdpqacp+rbk6GYwiGN/39PvPxeoqcLBJQtESt3IGYIR8+/E+J893ueCO9VVsLEB9TXvS8eYijVl10iHsIOUK/S0KPMoLfW0wuvKRgE0RzLD0d07wZGB3c6ULHUAcOWNxVllazHqbn0aqj+Ov/13RPzC+70TfV02gD2kVKGnVZlHaamnjxDfBsAlNbzv2BE0HRjcCWqBmioce0R26/lhc7+C8T97POGL81IFh8MW2NKXb2avN1s4hOWlTKGnZZlHaamnvLZ7iPQNyQx1f9sRl4/TWPkcjpT9KC4fa6AyJhXirLJyLfUYNR86CN/RI3IBiLKRZdwiF8AeUmKhQVqXeWe6+j1l8cPea2HQFqnxT7z7Dk688/e4fswxJd/D0BtujOvH7C+zuQnHfvZTNFY+1/FrmZMva/tv0ccBAM78sXDlxb5Tna99NhuuO4xQ7SGEj9SmxCp7Z1Y2zpkpeceHX6HikmsFA1ie7Qtdy/w0WuopicvLfgrgXyXGNkNBfLjpuQHfO++JkTMEZ5WtRcak8+L6cQfCt/tNZEw6L6Er4X2730SkuQn+PW8iUF0F356dCRsrUUYXXY7cj02SGp7hMM+nby8TX6VnVbYudC3zHmipp5S2Z89XHQYhT2L8E++9jRNv/yMhHztjUiHOWrUWRnZOQj6+1fl2v4lATRVatr1ii4KXn6XrznG9sW2ha5n3QUs9ZUhebudIBB9WPAszHPuOcP01bO5XdOU57LN9bd4nrsCQ8RNlBmf+Cy0suUpmcOuz5aI4LfMY6EK51GHgK1JDN3xYk9AyB4D6Z36LgPyzzuKMnCEYesONGPuDUnzs9y9gTMn3LLlo78Q7gkesEl3BPyuVv0djUbYrdC3zftBStz1et84Fpi9IjX/y/feSMo70o2xWEy338T97HON/9rj44sHOQi3NaDl8SGp4QsSYJzW41dmq0LXMB0BL3d7CDRdL3Ttv3PtB0jYU8e1+0xb3kCVkTCrEmJLvYeKTv8fQG260xBa2J95NzJqK2PAswcEtzTaFrmU+CFrqNmaIvXgla3Ye1fCMnr/RG1feWIwp+R7OeeIZjLj9TtEsgfp6+I/Hvp9/XDFdxQ89lCEzuLXZotC1zONAS92mZGYj/hMnEGpO7hatzdteQbiuNqlj2lF0b/qJT/5edG/6xn37ZAYmZMDhv05mcGuzfKFrmceRlrqt8LoHcsEksqK3af9eiWHRvO0VkXH7w7dnZ5cfUm9ConvT569YCVd+7BvfxMtgtwEeHLkrV1bmlA7Qm7a9e+kFLfM4Irqby707qbjk59JRVB8izutAELm02PSRzIu1f8+bwNwvi4xttjQjUPM+AtVVCNcdRqCmCsCpnd9i5cofC2feWDhyhsA96TxkTCqEM29swjbQyZl2DbKKLseRsv9I6hsijoTRfPAAcs46O2ljdhpdC70bli50ZBrXADxKOkbKYSoGoIVudSZfBUr+VhEthw4k/FG1nrQm8RCQQM378O1+E/49b6J195swm5vi8nFDtYdPbfV6WsFmTCpEZtHlHT/itaGOkTME+StWovH553DskZ/G7XPpS9P+vTKFzjiP1/x4JC387vHkD25d1i50wwxCz7WPP4JPOoKKAUHkcnvjfqF7o0DCi6hl+6to2f4Kmre9mrTS6yxQU4VATRXq2xcAZkwqxJAbbkRm0eVxmcEPbf9Ytd9f3nGFIZFaag8jEvDDkeFJ+FhdEBkg93QA/5fcga3N2oWe2fIaWnMOA0j+DaLUtkY6gOod/2qFB624MtnjmqGg5DPGCeHbsxNNz28UK/HeBGqqEHikrXhd+WOR+8WvYOjMGwc1c2+7t16Og0uLk1LqTQc+wjCJ/fgZ10ILvQvLT3/54ZXjQMbtIGQmeKiLAYxO8Bi9I2wHI5jQMUy8SveUvJTQMdSgSW332rR/b9yOSR2oghdej8vHaXz+OZx84he2POls6MwbMeL2f4EzL39QH+dI2Y+6nCSXCJmjxuCs6dckdIxuMXb///buPjzK8s4X+Pf3TCbJJDNJCElIeBMbRaVqaNpqlVaoPdJzlW63cq0vXQvtbu1BksApMoG6R46xbLfFBPVgAnbLuj1hd49ai9tuaZWtVmxh2z2nKNoXBan4goQAAZJJQt6e3/kjGRohJM9kZp77mcn3c11eeLXD3F81zG/u+7nv3y014bnuD+xd3p6hA5AVa98DsCHZ42hTw/cBGPipHGZg4C+H/nlporPM7G7vajV45zUQ9zEsuzOCU9sfR8fOHSlZyKPan92B9md3IFBRicKlXz17pWusSsLrzr5fsnQfb4UODEB8vqSNMSLBlfrkkz659dYBdwf2Ls8fWyOakBSXmxi2q9XcOXArGEJJ7bpx//72nTtw6Is3o605NWflI+netxeHVy9HS93acR+PKwmvQ3BecucqZ9qM7E3z4ejb7Os+DAs6kSep6wW9r6MDAz09bg8LIHo3ehP8U2LfLtNz8AAOh6vQWr/ec8/IEyWyexfevmsJ2rZtHdfvLwnfm9SLXrqOHU3ae49KlEvuw7CgE3mM1tVZEFzl9rjGPpQBlNVtGFfBadu2Fe/ctSTms+KpyI50oK15K965a2nMt9Od/cKUpAY03ceMPaphQR+GBZ3IayYHZwOS4/awXYY+lAuX3hnzs3O7M4LD4Sq0NY9vxprKeg7ux+FwFdp3xvZc3AqGzj5TT7QzbW1QE70LxMyjKa9iQSfyGkPLiF0GWpgGKipjvmik5+CBCTMrvxA70oHW+vVobVgf0+8LVFSiYPHtScnUfdzIZS0s6MOwoBN5T3xnlcahLxKBDri7WXg8m+Ciz8vTZdNbvNqf3YGWurUx/Z7CJV9JytL7mZMGNsYpyrWuzvOntdzCgk7kNSKz3B6yt6Pd7SFRsPi2mDbBRYt5um58G6/I7l0xzdSTtfTe2+Hu7XwAAJEMTMk30Uzek1jQiTxH3S/oLhdJf2lZTEvtLOaja392R0xFPdpLPpH6TP236e93/c+LV7GgE3mNuj9D73N5hj4phmJud0bQUreGxXwM7c/uiOlYW6x7F8bSc/pUQt/PMctiQR/Cgk7kNYJyt4fs7XCvWPpLy5C3cJHj17fWr+czc4famrei+5WXHL02GbP0/q6uhL6fI6oXuz+oN7GgE3mI/mNdNoDE3KkZg57Tp10bKxRDMW/fucPVO77TQWv9N2B3OnueHct/CyeMLLuLTnF/UG9iQSfykq6cAreHHOjpgQ70uzae0yJid0ZwfMvDSU6Tfvpajpy9nnUswetvSOjYbu/FGCSu/5nxKhZ0Ii+xLdc/nNxcJs0qn+14Z/up7Y/zufk4ndr+hKPe71YwlNA+731dnQl7L8cULOhDWNCJPEVdP4Nuuzg7z53nfEZ4avsTSUyS3uxIB9p3/tjRa3MSOEu3e5N7+/PIlAV9CA/kE3mJTwqg7g7pZkOZQMWHHb2ufeeOhM3OrWAIWR+4BADQ39oS9wY7f2kZMkoGv3f1/PGNuHNmlc+GlZsLAI43tDnRsXOHo53sWeWJu7BsoNdA+1egyMSgXsSCTuQltmZDxNUh3Xx+7vRe7649L8Y/1lBb2XN3cvcdPYITWx6OebNdcN58TF7+tfMeGXTv24u2bVtjbkVbuOROFCy+DVYw9L7/vX3nDpzcFv8VsH0tR9D9yktj/jvPKp8NKxhKyBco20Q/d4jrm0i9ikvuRF4iVrbbQ9r97szQY2k3Gu/O9rxPL8K0hs0jHsvyTylDad2GmNrOltSuQ2ndhhGf/wcqKjGtYTPyPu1ss58VDGHGo80oXHrnecUcAPIWLsKMLc0Jue60e99vHL0uUbN0u8/EBS3q+p8Zr2JBJ/ISAx9OtktL7hkON8PFejXouQIVlY5am+YtXOToopKCxbc7OjdfEl7n6Fx30fKvjVmso9edjlTwY+F01SBRd6WbeYZOUSzoRF5iu1/Q3Vxyd6L/aHxLzbHcJpa/+LYxX1O45CsJGzuWpjpWMBRTA56ROP1yZAUTs2o90GegoKtwhj6EBZ3IS8T9Dye3NsX5HM42ew7uj2uc3Bh2bfunlI06O40+X07U2LnXx3ZELDfOI2VuH/szs+SOLPcH9SYWdCIvUT3j9pCS4c7eWKdL7m4bbXY6npnraF8AYn2/jCmun2KkFMaCTuQllrhe0C2fOwU93pl3qkjkrNiOGLiSNA6W3+/+oIoe9wf1JhZ0Ii9RAwXdn16nV510SHv/6y/8zD7W5/lj9VDvjXHDX7z7Cdxm+TPdH1TcX9XyKhZ0ognO8hmYVY3CafOZC3HaIQ0YbOQy2nnvvpYjMe26H+u4Xde+vY4vTgGAzj3xHd9L9G1qY7FcenzzPga+BHsVC3qUqm06AqwMn+kIZJja7s/QXfoQdnyEaqir23g57WMOAMc3PzT2a7aM/RpgcHZ+coz7yO1IB1rr1zt6v+5XXkL7szscvfZCnB5Hi3Xl4EKMFHSABX0IC3qUiJGehe/Xz45HE53oKdeHdHHJ3cls1wqGYmpCcy470oEj960ZdSy7M4LWhvWOnut379uL1ob1o86s7c4IDq+uctTdLbJ7F1obRi/qPQcP4Mh9a8Z8r7FkOmwYk6j9DUYKOpfcz0qvh2fxUO11u+Xm+Xws6BOd+E5B3W3m7uaHcP/RI466kuVeP9/xFaAj6Tm4H4fDVShYfBvyFn727G5xuzOCyO5dMbdWbX92B7r37cWkJXcip+LDZ9+v/2gL2nf+GKe2PxHTZrj2Z3egr+UIChbfjkBFJazc4FDuAzj99ONxz8yjnFyPandG4m4zG2VmyR2ufwn2Khb0KIEHWhyxJ/GEN6Cn3F4382W6d4y3c88uR+fEQws/E1dBBwZn6m3NW9HWPPoyuFN9LUccL5c70b1vb8z932OR9+lFjs7Qx9uZbzhfloEeL4LYdkGmMS65/4n5JXcb8fV5pNTX73P9w8ny++HLcqeoR3Y7u3Qlq3y26xu60k3oJmdd5jrj7Js/nD9k5COMBX0IC3qUSrfpCIDNGfoEJ6tWnTJxrtYfZ89wp+xIh+MZoZOrP2lkgYpKx1+I4t1JP1xmMC9h7+UYl9zPYkE/S0+YTgDhkjsBgB5ze8RMF2dWp592tpQeqKhEMM7WpxOV05vkeg4eSNjzcwDIzDMwQxdx/c+LV7GgRwnaTEcAdJbpBOQBgoNuD5np0gwdGFx2d3oWuyR8b9w3jk00hUvvHPGa15F07EzM5ruojEBOQt/PEQN/XryKBf0s8cIM/TLTEcgDVA65PaSbzz7tSIfj+86tYAgl4XuTnCh9BCoqHT+qsDsjaE9gQc/Mz0/Ye8VEbdf/vHgVC3qUrV6YoSfmUmJKbaKuf0C5/ezz+JaHHc/Sg/Pmo3Apn6ePxQqGUFa3wfHrT21/PKF95408PweAXj8L+hAW9Cif7YGmyXKl6QTkBZb7M/RgEGK593FgRzpiOpZWuORO5H06vrvB05kVDGFaQ5PjxxN2ZwSntj+R0AyZeSZm6HpaVq3iprghLOhRvoJ3TEcAAN3yEJ+jT3Rq/8HEsNmFRa6Od2r7EzH1NS8Jr2NRH0G0mDtt8woAbc1bE35XeqDI3Z+fQfI7A4N6Fgv6EFm2rAvQVtM5YPdx2X2i68t43cSwgeJiV8eLpa95VEl4HQoW35akRKknq3x2zMW8+5WX4m7aM5JAkbs/P4P0VQODehYL+nAGNiOdRyS+q6Yo5Q2dRT/q9rgmPpAju3ehc4+zZjNRRctXOT6Wlc7GU8ztzgha67+R8CyBopKEv6cjitfMDOxNLOjv4/5mpPMjYIHpCOQJL7s9YKCo2NXn6FFH69fHfId53sJFcV3gkuoKl9yJGY82x3yk7/iWhxJ67jwqUGyooIuyoA/Dgj6cwMhS5znGbnRNE4C6XtAB95+jA3+6HS1WscxM04W/tAwzHm0e167/9p07Enbpy7lyjCy3AzDwxdfLWNCHU/zWdARAsrWx/lrTKcgwy8zPotvP0aN6Du4f80rRczm9GjQdWMEQCpfciYu2PT2uLzLtO3ck9GKZc2Wb2BCnekKq17CP+zAs6MNliAcKOgBw2X3Ck4xfmhg2x9TSKQavFD2+5WHHr89w2A0t1eUtXIRZ27aP+yx+z8EDMf17jZW55XYY+TPiZSzow8hd4d+bzgAAEGED6wlOlq86BMVbbo+bPbnItZvXRhLL7mt/6dQkJjHr7Iz8n55GSe26cbe/7Tl4AIfDVQk/ojZcaPqMpL33qBQvmBnYu1jQz6OvmE4A4BP64IMB0yHIOCMfWKEZF5kYljC4L6Ckdt3ZGbnTnuwjad+5A+/ctSSpxRwAQjNmJvX9L0iUBf0cGaYDeNCvAVxtOEMQmQN/DiDxh0UpdVj4FRRfcnvYvFkX49Qb+90eNmY9KZDRCX9pGXKvvwGhhYsSttEv2c/Mo4LTZkB8BsqIog3Hu7ww+fIUFvRzqfUriH7VdAxA7gAL+sSmA7sAn+vDZobykJVfgJ7T3u6oaXeOf+ZpBUPIW/gZdO97CT0H3f1iYAVDCFz9IQQqKpE7b35cs/BzDZ4zX+/48pt45c001NhS8KLU1dlmBvcuFvRzSf9/mPgQPT8HPqubvzVJqu45aToKmSHVa/+gjQ1vQeD6Gnho5kXoedX9gh6oqHT82v6j4ztPPVKr1O59e9G9by/6jx5BX8t76H7lpXG997n8pWXIKClFoOLDyCgtQ1b5pUk7btf9yktorf9GUs6Zj8SXmYmc0lJXxjqPqjvfWFIMC/o5hj5E2yEwdHXQMOr/AoDNpmOQQaLPALLM7WFDM2bi+Kv73B42tham+/bG/P4X6nseqKgc8ctEdIy+o0fQ76BQRt8jo7QsoTPvsbRt24q25q2ujQcY3muh8oy5wb2LBX0kor8AxAu3QNwBFvSJTeQZKFwv6L6sbOSWlqHTpdleVGjhZxy9zu6MxDwTHc8lJtEC7dUdqm7PyofLm2VouV3xlqwIs0PcCLjLfSQiz5qOMOR6bdpwhekQZFCP7wUAamLowis+6Op4/tIyx8U21mfEWeWzMePR5rTpLtd/tAUtdWtxePVyI8U8t2wqMvMKXB8XwNCqFY2EBX0klu2hHxjr66YTkDmDF7Xoz02MnVUwCTklU1wbL//m2x2/tiuGC10CFZWY1tDk6hJ4svQfbUFrw3oc+uLnXdv4NpLCy+cYGxsiPzQ3uLexoI9A7lpzAKrvms4xSJbqIxvSt4MGjc2S75sa2q0P7uiucyfszojjYlaw+DZMa9g87sYsXjG8kCerH7tTuaVTkVUwydDo2gFf6GeGBvc8PkO/EJEfAagyHQMAYFn3AFhhOgYZova/AtZmAOL20NmTixAoLkH3sdakjlO0/GuOi66TbnL+0jKUhNfFtGvei9p37kDHzh3j2gCYLIVXGJydq2yXZcv6zAXwNs7QL0Rlu+kIfyI1ummTseuMyKzBCyg0tkvDE2hykp+lZ5XPRt5C53tQT21/YtT/v2DxbZixpTlli3m09/ofb74JrfXrPVXMc6aUGZydAxCbvTlGwRn6BUjN6ue0saENgkLTWQAAVu/XAPwP0zHIEJHHoTDS4z97chECRcXoPn4sKe9fUnuv49e279wxYivT6JJ9/uLbU/JZeeeeF9G5Zxciu19MeqvWeCT7y92oFEfhz3/OXADvY0EfjegPAPFA1zgAol/T7zzUKMtWub+llczrz/wBrJ4GiOSaGL7o6rl45/l/T/z7Ll8V087zk9v+dNbaX1qGwNWVyLn+BgTnpc59RnZn5Gwjm56D+z01Ax9NaMZFyJpkcnaOx7ncPjoW9FHpU54p6JAc9PU/COALppOQ+2TlymPa2PAU4H5vdwDIyi9A/sXlOP3mwYS9Z3DefBQsvs3x6/uOHkHopkUIVFQmtHHL4BL3Q4Nd3aYM/uUvnYqs8kth5QbH/b7RbnM9b+xH/9Ej6Dm4f6gTXep9J5eMDBRdVWE4hf09wwE8z/VNNqlGG+tbIeKd59diLZCqu9n2cALSR+oXwBIjR9gAwO7txaGdP4HdF/8kKat8NqY1NBnffe70EpNosR9LqhbssRRdVYGCSwye4Vfsk5rwXHMBUgNn6GMRaQaw2nSMs2z7UQBsNjMR1YR3oanhTYhcbGJ4KzMTkz94NY69/Jv43icYQun9G4wX81japfa1pGehdiIjJ9dsMQcAKGfnDnCX+1hsuNsgeSyCy7WpYZXpGOQ+EVFY+K7JDPkXfwCZ+fnj/v3R9qsmN67ZnRG01K11vfd5qppS+WGzARTd8Ms/mQ2RGljQxyArwq9B8Z+mc5zjG7ppw3TTIciE/keh6DaZoGTuR8b1+8bTSz3ROve8iENfvNlol7VUEpw6DYFi97oFjki0WZaFj5sNkRpY0J0Qfcx0hHMEYfn+2XQIcp9U3XMSos0mM2QXFqLg0tiKsuliHu20duS+NZ4+FuYlvqwsFM81fpZfodaDpkOkChZ0JzLytkHRbjrG+whu0KaN95mOQQaI/RAMXdgSVXRlBbInOWvRYLKY250RtG3birfvWmK8ZWqqKfvYPPiysg2n0B9Jzer9hkOkDBZ0B2TZsi4I/sF0jvNpnTY23GA6BblLqta+DuiPTOcou24efJljf+DbkQ6cfvoJ9Bw84EKqQf1HW9C2bSsOffFmtDVv5aw8RkVXVSC7cLLpGIBY3zYdIZXw2JpDuumBcvisN0znOJ+2QPrnSNU9J00nIffopo0V8OnLpnOcaTuBd3c97/j1WeWzEVq4CMF585ExpTTheaId1zgbH7+c0lJMve4TpmMAihekJvxJ0zFSCQt6DLSp/keA/JnpHOfTH0p17edNpyB3aVPD4wCcd2ZJkpP7X8OJ370a8+/LKp+NQEXl2b/G08Sl5+ABdO/bizOv7OVGtwTw5+Ri5qdugmT4TUcBIPOkevUe0ylSCQt6DPSRB+bBsn5pOseIFE1SE64xHYPco4/UXwxLDgDwmc5y5Fe70XnkvbjewwqGkFV+KXzBEDLLL73g66KtUlOlZWqqEF8GZiy4EZl54z+WmEBPSHX4dtMhUg0Leoy0sf45iNxoOseIFPdJTfgbpmOQe7Sp/lFAlpnOAQDvvvhznDnB00WpavoNn0T25CLTMQBgAJbvElm+6pDpIKmGm+JiZVnevfFMcL9ubrjLdAxyk9aZThA19bpPwB8cf+9zMqfsunleKeYA9Hss5uPDgh4jqVr9KwDevcJPsUWbGniBywQh1WtaoLrBdA4AsPwZmP6JBfBlmz7qRLEoqfwockunmo4xSNGDgax7TMdIVSzo4yHi/AJnM/5FN2+8xXQIcomd9XeAtpqOAQC+7ACmf3wBLE9sqqKxFF7xQeRdNMt0jGH0YVm58pjpFKmKBX0chmbp3u7Upvoke75PDLJyZTtEPNNkyB8KYdrH50N8vPvJy/Iv/gAKL59jOsafqB4b/HJK48WCPl4ZvlpAu0zHGMOD2li/2XQIckHRzO8C+lvTMaKyJk3C9BsWwPJzpu5Fky69DMVzDV+6ci5L/qesXOmtjpwphgV9nGTZqiOA3G86x5hElmtT/b+ajkHJJbfeOgDIctM5hssqmIQZCz6FjEDAdBQapnhuJSZfebXpGO+nuhutkb83HSPV8dhanLSp4QCAS0zncOBX0N7PSs3fnDAdhJLHS8fYoga6u3F4zy/Q237adJQJr/Sa6xCc5rGLGlV7YescWbnmoOkoqY4z9HippMoxsY9BMvfplo0fMh2EkiknDMBTLYp9gQCm33CjN3qDT1DiszDtEwu8V8wBQOQ+FvPEYEGPk9Ssfg7A903ncGgabN2rjQ94ammWEkeqqyMA/sp0jnNZ/gxMn38jgtNmmI4y4fiysjD9hhsRKCo2HeV8qrtxLPKA6RjpgkvuCaDfeagM/f1vAJJjOksMnkKPtVTuvrvbdBBKPG1qeBjAfzedYySn/3gQx9i21RU5JSUo/eh1sDIzTUc5n2onFFfJito3TUdJF5yhq9cenwAAC4ZJREFUJ4AsW3UECs907HLoL5A18BvdvOEy00EoCYoja6CI/cYUF+R/oBwzP3UTMnJS6ftv6im6sgJT5833ZjEHALFqWMwTizP0BNKmhl8A+LjpHDFT1KNb75fa2k7TUShx9JEHr4IM/AdEck1nGYnd14/Wvf+JyHuHTUdJKxmBAMqunYesSZNMRxkNL19JAs7QE8q+BUDq3U4hqEUA+7Wp4Q7TUShxZMXdr8KSsOkcF2L5M1B67fUonltpOkrayC2dipmfWujtYq76JqSP+3iSgDP0BNPGjZ+C6M9M5xg31V8Dvq9Izd2/Mx2FEmOwD4H8uekco+nv6kLrS/8PXa1HTUdJSRnZ2SiuqETu1Gmmo4ylD7YulBW1L5gOko5Y0JNAm+rrAe/OjBz6P7Ctb8mKuz35HJac04ceKoB/YDcEHurzObLO9w7j2L696D9zxnSUlFFwyWxMvuJKSIbPdJSxqa6SmtqHTcdIVyzoSaKNDb+G4BrTOeKm+DEs+eZQ/3pKUfpowxwM6P9NhZMY2j+AE3/4LU69sd90FE/LKijElI98FJmhPNNRHNJ/k+raz5lOkc5Y0JNEmzbOgOorEBSYzpIgP4egXqrCPzUdhMZHmzZ+GdB/NJ3Dqd6Odpz47avobHnPdBRP8WUHMPmKOcib9QHTUZxTvIU+31xZteqU6SjpjAU9ibRx42cgusN0joRSPQbBdqj1/aGmOpRCvHw+/UJ6O9px8rXfo+Pdd0xHMSozLx+TLrscoekzTUeJjaIdan2cj++SjwU9ybSpYQOANaZzJIeeBOQJKLZLTfjfTaehsWldnYWi4DMQ3GQ6S6z6u7tx8vXX0P7Wm1B7wHQc1wSKijFp9uXImVJqOsp49EH0M1JVm7obhVMIC7oLtKnhSQC3mM6RVKqdEDwP1Z9C5Rk2jPAu3bQpD76eXwDisSu3nLF7e3Hqj2+g/c2Dabt5TiwLwenTUVA+G1kFHj6CNhbFl6Um/L9Nx5goWNBdoo31z0HkRtM53KMHoPgpRF6HyttQeQtnBv7I5jXeoJs2TIdlvQiRi01niUf38WPoeOsQOt57F9rfbzpO3AJFxQjNnIXQ9OkQX4bpOPFR/K3UhNeZjjGRsKC7ROvrcxHAixCZ2F00FO0QfRuKVkC6AO2CSBdUuwd/RSdE1XTMMSlek5rax03HiIc+Un8xLNkNoMx0lnjpwAAi772L9rfeQvex1DrL7s8NIm/mLOTNmgVfdprcHa94TGrCXzEdY6JhQXeRbn2wEGfsFyC4ynQWipf+UKprP286Rby0acMVgO85pEFRj7L7+tB9/Bi6jx1F9/Hj6DntrY3VGdnZCBSVIFBcjEBRCfzBoOlIiaV4DMcjX5W6Ott0lImGBd1lLOrpIj0KOjBU1NX3SwgKTWdJBruvD2dOHEdX61GcOXkCPadPQQfcqzX+YAjZkwoRKCpGYPJk+FPm3Pi4PIVjkdtYzM1gQTeART0dpE9BBwDdsvFDsO3nAEnhHVjO9Xd2obfjNHraT6O3ffDXvo4OqD3+OuTPyUVmXj4y8/KQmZ+PrFA+MvPzE5ja856S6nB6b/71OBZ0Q3Trg4XosX8G4EOms9B4pFdBBwBtemAu1HoGgimms5hi9/XB7u3DQF/P4N/39WKgt2/w7+1++PyZsDIz4cvMhJXhH/zVnwlfVpbp6IZpM451fkXq6lJ/Z2IKY0E3SL/z7Xz0+Z6f8BvlUlL6FXQA0M0bLoPt2zWRizrFSptRFf6yiHh/M2ua4/WpBsmyr5+Gf+DGwRvOiMyTqrWvwxqYD1X2W6WxKR6T6tovsZh7Awu6YbLs66chOf+FRZ28QqrWvg5/xkcA8EIeupABAGEeTfMWFnQPkOrqCPx5NwL6Q9NZiABAlq06guLIfCi2ms5CHqN6ArYulOrwRtNR6P34DN1jtLHhbyD4pukcNJb0fIY+Em2q/yogf286B3mBvgyVz0tN+C3TSeh8nKF7jNSE/w4qiwBETGchAgCprv0uIPOgesJ0FjJJf4iMvHks5t7Fgu5BUrP6J5CBjwD6uuksRAAg1av3wJfxESheM52FDFDdgKrwzbJsWZfpKHRhLOgeJVVrX0cXPgzFj01nIQIAWb7qEOzMawHlVZgThWovgC9KTe3XuZPd+1jQPUxqazulJvxnUP266SxEACArV7aj+KL/Cui9APpM56Fk0tdhW9dIdfifTSchZ1jQU4DU1G4YfIYJPrsi4+TWWwekuvabsORaAC+ZzkMJNwDVDcjpnCsrV+8zHYac4y73FKJNTUFo1yaI/JXpLDRxdrmPRZsavgWAq0jpQLEf0KVSU8u+GCmIM/QUItXVEamp/WuoLuaOY/IKqQ7fA9WPQcHZXKpStaH6IOzMq1nMUxcLegqSmtqnYWddAeCnprMQAYDU1P4a/tBHAb0ffLaeYvQA1L5WampXy8qVPabT0PhxyT3FadMDSwHZBMiEuqfRPC65X8jgrW3yKESuNZ2FxvRtqQ7fYzoEJQZn6ClOqtc0w7bnAPi+6SxEACDVa15Gdfg6iP41FEdN56ERqP4A4itnMU8vnKGnEW2svxbA/+LMyA2coTuh/7AhhG7rHkDuhmCiXxpunuI1WNZdUnX3LtNRKPFY0NOQPrLxc7DsbwNyheks6YsFPRb6nW/PRF/GfYAuhUiG6TwT0BuAvR7Huv5F6ur6TYeh5GBBT2Pa2PAlAPdDcJHpLOmHBX08tOnBS6D2PSzsLlF9G5Bv4njkMRby9MeCPgHo5oYVUL0XkBLTWdIHC3o8dNMD5bBkNQRfAiTHdJ60o/g9IBulZvVjpqOQe1jQJxBtbFgC6DKIzDOdJfWxoCeCbv7WJCDjLtiogchU03lSnAL6Y9h4WFbUPm86DLmPBX0C0kcb5qBfawC5A4I803lSEwt6omlj/c2AfBmCz5nOklJU3wOwDeLbKtV3v2E6DpnDgj7BaVPDHVD8NwhuMJ0ltbCgJ4tuqS/BAL40VNznmM7jSYO3oP0bYH0Pxzt+InV1tulIZB4LOgGIblYauBMifwlghuk83seC7gZtfKASYi0F9AvcAwIA2ANoM6T/Sam656TpMOQtLOh0Hm18oBKQv4DILQAuMZ3Hm1jQ3aabGz4PxR2A3jSxOiPqbwHrKdh2s6yofdN0GvIuFnQalW7ecBngWwjVmwAsACRkOpM3sKCbok8+6UProQoIboTKJyFyA4Cg6VwJ9AYUzwP6c4i+INVrWkwHotTAgk4x0UcemAfLmgfVayByDSbs8jwLuldoXV0GikPXQHUBRD8J4PoUOwp3CMALULwAe+A5Wbn2XdOBKDWxoFNcdNOmYlh910LsjwG4FsBHJ8ZyKAu6l2lj/XWAdQVgz4bIZVDMNr7BTvUYgP0A9kNkPwSvQXwvy/JVh4zmorTBgk4JN3Qs7lJAp0JkGiDTAJ0KyCQoQhCEAM1L7eV7FvRUpI/UXwxLL4X6LgXs2QAugWA6FGUQKY7z3c8A0gLgPQBvQrEfggOwBw5AA/tl5cr2BPwjEF0QCzoZpaqC++8f/DmcM0fw+9+nxs/knDkqt946YDoGJZbW1Vkx/xzOmaO45RZbRDSJ0YiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIAPx/0G/opjoIZkQAAAIUaVRYdFhNTDpjb20uYWRvYmUueG1wAAAAAAA8P3hwYWNrZXQgYmVnaW49J++7vycgaWQ9J1c1TTBNcENlaGlIenJlU3pOVGN6a2M5ZCc/Pgo8eDp4bXBtZXRhIHhtbG5zOng9J2Fkb2JlOm5zOm1ldGEvJyB4OnhtcHRrPSdJbWFnZTo6RXhpZlRvb2wgMTAuODAnPgo8cmRmOlJERiB4bWxuczpyZGY9J2h0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMnPgoKIDxyZGY6RGVzY3JpcHRpb24gcmRmOmFib3V0PScnCiAgeG1sbnM6cGRmPSdodHRwOi8vbnMuYWRvYmUuY29tL3BkZi8xLjMvJz4KICA8cGRmOkF1dGhvcj5SQVZBTCBQUkFKVkFMIE48L3BkZjpBdXRob3I+CiA8L3JkZjpEZXNjcmlwdGlvbj4KCiA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0nJwogIHhtbG5zOnhtcD0naHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wLyc+CiAgPHhtcDpDcmVhdG9yVG9vbD5DYW52YTwveG1wOkNyZWF0b3JUb29sPgogPC9yZGY6RGVzY3JpcHRpb24+CjwvcmRmOlJERj4KPC94OnhtcG1ldGE+Cjw/eHBhY2tldCBlbmQ9J3InPz6cbDvxAAAAAElFTkSuQmCC'
                        updatedAt: '2021-11-04T15:00:22.622Z'
                        status: auto_enabled
                        languages: {}
                      - id: 21b7d3ba-031b-41d9-8ff2-fbbfa081ae90
                        version: 1.2.3
                        requiredApiVersion: ^1.17.0
                        iconFile: icon.png
                        author:
                          name: Rocket.Chat
                          homepage: 'https://rocket.chat/'
                          support: support@rocket.chat
                        name: Dialogflow
                        nameSlug: dialogflow
                        classFile: DialogflowApp.js
                        description: Integration between Rocket.Chat and the Dialogflow Chatbot platform
                        implements:
                          - IPostMessageSent
                          - IPostLivechatAgentAssigned
                          - IPostLivechatAgentUnassigned
                          - IPostLivechatRoomClosed
                          - IUIKitLivechatInteractionHandler
                        commitHash: 10677db664589b7bc9bc244f9aa186c5923cb2ae
                        iconFileContent: 'data:image/png;base64,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'
                        status: auto_enabled
                        languages:
                          en:
                            bot_username: Bot Username
                            dialogflow_bot_id: Bot Id
                            dialogflow_bot_id_description: Select the bot to use from the list of bots. Use comma to seperate values in respective fields
                            dialogflow_project_id: Project Id
                            dialogflow_bot_list_config: Dialogflow Agent Configuration List
                            dialogflow_bot_list_config_description: An object containing the Omnichannel bots and the configurations necessary to reach the corresponsind DF agent endpont
                            dialogflow_client_email: Client Email
                            dialogflow_cx_agent_id: '[CX ONLY] Dialogflow Agent ID'
                            dialogflow_cx_agent_id_desc: |-
                              1. Go to the Dialogflow CX console. 
                               2. Select the project. 
                               3. From the agent list find the right agent and click `⋮` . 
                               4. Select copy name. 
                               5. The agent name has the following format: 
                               6. `projects/PROJECT_ID/locations/REGION_ID/agents/AGENT_ID`. 
                               7. Copy `AGENT_ID` and paste it here.
                            dialogflow_cx_fallback_events: '[CX ONLY] Fallback Events'
                            dialogflow_cx_fallback_events_desc: Dialogflow CX does not support fallback events. Enter a list of event names that will be treated as fallbacks from the app.
                            dialogflow_cx_region: '[CX ONLY] Dialogflow Region'
                            dialogflow_cx_region_desc: |-
                              1. Go to the Dialogflow CX console. 
                               2. Select the project. 
                               3. From the agent list find the right agent and click `⋮` . 
                               4. Select copy name. 
                               5. The agent name has the following format: 
                               6. `projects/PROJECT_ID/locations/REGION_ID/agents/AGENT_ID`. 
                               7. Copy `REGION_ID` and paste it here.
                            dialogflow_default_language: Default Bot Language
                            dialogflow_private_key: Private Key
                            dialogflow_environment: Environment
                            dialogflow_environment_description: Name of the Dialogflow environment. Default environment is draft
                            dialogflow_fallback_responses_limit: Fallback Responses Limit
                            dialogflow_fallback_responses_limit_description: The app will automatically trigger handover if consecutive fallback intents are triggered N no of times. This setting defines this value N
                            target_department_for_handover: Target Department for Handover
                            target_department_for_handover_description: 'Upon bot-to-liveagent handover, the visitor will be transferred to this Department'
                            dialogflow_handover_message: Handover Message
                            dialogflow_handover_message_description: The Bot will send this message to Visitor upon handover
                            dialogflow_service_unavailable_message: Service Unavailable Message
                            dialogflow_service_unavailable_message_description: The Bot will send this message to Visitor if service is unavailable
                            dialogflow_close_chat_message: Close Chat Message
                            dialogflow_close_chat_message_description: This message will be sent automatically when a chat is closed
                            dialogflow_hide_quick_replies: Hide Quick Replies
                            dialogflow_hide_quick_replies_description: 'If enabled, then all quick-replies will hide when a visitor clicks on any one of them'
                            dialogflow_handover_failed_message: Handover Failed Message
                            dialogflow_handover_failed_message_description: The Bot will send this message to Visitor if the handover failed because no agents were online
                            dialogflow_enable_chat_closed_by_visitor_event: Enable Dialogflow Event When Visitor Ends Chat
                            dialogflow_enable_chat_closed_by_visitor_event_description: 'If enabled, then a dialogflow event will be triggered when visitor ends chat'
                            dialogflow_chat_closed_by_visitor_event_name: Dialogflow Event Name When Visitor Ends Chat
                            dialogflow_chat_closed_by_visitor_event_name_description: The bot will trigger this dialogflow event when visitor ends chat
                            dialogflow_enable_welcome_message: Enable Custom Welcome Message
                            dialogflow_enable_welcome_message_description: 'If enabled, then a custom welcome message will be sent when bot is assigned to any visitor'
                            dialogflow_welcome_message: Dialogflow Message to send on start
                            dialogflow_welcome_message_description: Custom welcome message to send to visitor
                            dialogflow_welcome_intent_on_start: Send Welcome Intent
                            dialogflow_welcome_intent_on_start_description: 'If enabled, then a welcome event will be sent when bot is assigned to any visitor'
                            dialogflow_enable_customer_timeout: Enable Customer Time-Out
                            dialogflow_enable_customer_timeout_description: Indicates whether chats are ended if the customer doesn’t respond within a specified period.
                            dialogflow_customer_timeout_time: Customer Time-Out Time (seconds)
                            dialogflow_customer_timeout_time_description: Sets the amount of time that a customer has to respond to an agent message before the session ends. The timer stops when the customer sends a message and starts again from 0 on the next agent's message.
                            dialogflow_customer_timeout_warning_time: Customer Time-Out Warning Time (seconds)
                            dialogflow_customer_timeout_warning_time_description: |-
                              Sets the amount of time that a customer has to respond to an agent message before a warning appears and a timer begins a countdown. 
                              The warning disappears (and the timer stops) each time the customer sends a message. 
                              The warning disappears (and the timer resets to 0) each time the agent sends message. 
                              The warning value must be shorter than the time-out value (we recommend at least 30 seconds).
                            dialogflow_customer_timeout_warning_message: Customer Time-Out Warning Message
                            dialogflow_customer_timeout_warning_message_description: Enter message to show to user as idle timeout warning. Use %t as placeholder for count down.
                            dialogflow_session_maintenance_interval: Session Maintenance Inverval
                            dialogflow_session_maintenance_interval_description: The bot will send session maintenance event to dialogflow at every interval. The interval is a human-readable format String (i.e. 8 minutes). Session Maintenance is for keeping long running dialogflow sessions active.
                            dialogflow_session_maintenance_event_name: Session Maintenance Event Name
                            dialogflow_session_maintenance_event_name_description: The bot will trigger this dialogflow event for session maintenance
                            dialogflow_log_level: DialogFlow App Log Level
                            dialogflow_log_level_description: Redeploying app or restarting server is required to apply changes
                    success: true
              examples:
                Get with no Query Params:
                  value:
                    apps:
                      - id: 0d3ac5b3-dd0b-43d3-924a-5a7433902589
                        version: 1.0.0
                        requiredApiVersion: ^1.17.0
                        iconFile: icon.png
                        author:
                          name: Rocket.Chat
                          homepage: 'https://github.com/RocketChat/Apps.Salesforce.LiveAgent'
                          support: 'https://github.com/RocketChat/Apps.Salesforce.LiveAgent/issues'
                        name: Saleforce Live Agent Integration
                        nameSlug: salesforce-live-agent-integration
                        classFile: SalesforceLiveAgentApp.js
                        description: Integration between Rocket.Chat and the Salesforce Live Agent (Chat). Please refer our Github repository for setup instructions.
                        implements:
                          - IPostMessageSent
                          - IPostLivechatAgentAssigned
                          - IPostLivechatAgentUnassigned
                          - IPostLivechatRoomClosed
                          - IRoomUserTyping
                          - IUIKitLivechatInteractionHandler
                        commitHash: 947b904c7e5fe7512fb0d7df174a2ffc0ee02397
                        iconFileContent: ''
                        updatedAt: '2021-11-04T15:00:22.622Z'
                        status: auto_enabled
                        languages: {}
                      - id: 21b7d3ba-031b-41d9-8ff2-fbbfa081ae90
                        version: 1.2.3
                        requiredApiVersion: ^1.17.0
                        iconFile: icon.png
                        author:
                          name: Rocket.Chat
                          homepage: 'https://rocket.chat/'
                          support: support@rocket.chat
                        name: Dialogflow
                        nameSlug: dialogflow
                        classFile: DialogflowApp.js
                        description: Integration between Rocket.Chat and the Dialogflow Chatbot platform
                        implements:
                          - IPostMessageSent
                          - IPostLivechatAgentAssigned
                          - IPostLivechatAgentUnassigned
                          - IPostLivechatRoomClosed
                          - IUIKitLivechatInteractionHandler
                        commitHash: 10677db664589b7bc9bc244f9aa186c5923cb2ae
                        iconFileContent: ''
                        status: auto_enabled
                        languages:
                          en:
                            dialogflow_bot_list_config: Dialogflow Agent Configuration List
                            dialogflow_bot_list_config_description: An object containing the Omnichannel bots and the configurations necessary to reach the corresponsind DF agent endpont
                            dialogflow_log_level_description: Redeploying app or restarting server is required to apply changes
                    success: true
                Get with appName === ""  Query Param:
                  value:
                    Saleforce Live Agent Integration: 0d3ac5b3-dd0b-43d3-924a-5a7433902589
                    Dialogflow: 21b7d3ba-031b-41d9-8ff2-fbbfa081ae90
                    success: true
                Get with appName === "Dialogflow" Query Param:
                  value:
                    Dialogflow: 21b7d3ba-031b-41d9-8ff2-fbbfa081ae90
                    success: true
      operationId: get-''
      parameters:
        - schema:
            type: string
          in: query
          name: marketplace
          description: '[Pre-existing] Gets all apps from the Marketplace'
        - schema:
            type: string
          in: query
          name: categories
          description: '[Pre-existing] Gets all categories from the Marketplace'
        - schema:
            type: string
          in: query
          name: appName
          description: IF (value === '') Gets name and id of all apps ELSE Gets name and id of the app with the same name as the value
      description: 'This endpoint returns apps, either installed in this instance of RC, or marketplace apps.'
components:
  schemas:
    User:
      title: User
      type: object
      description: ''
      examples:
        - id: 142
          firstName: Alice
          lastName: Smith
          email: alice.smith@gmail.com
          dateOfBirth: '1997-10-31'
          emailVerified: true
          signUpDate: '2019-08-24'
      properties:
        id:
          type: integer
          description: Unique identifier for the given user.
        firstName:
          type: string
        lastName:
          type: string
        email:
          type: string
          format: email
        dateOfBirth:
          type: string
          format: date
          example: '1997-10-31'
        emailVerified:
          type: boolean
          description: Set to true if the user's email has been verified.
        createDate:
          type: string
          format: date
          description: The date that the user was created.
      required:
        - id
        - firstName
        - lastName
        - email
        - emailVerified
  securitySchemes:
    API Key - 1:
      type: apiKey
      in: header
      name: X-User-Id
    API Key - 2:
      name: X-Auth-Token
      type: apiKey
      in: header
security:
  - X-User-Id: []
  - API Key - 2: []

```