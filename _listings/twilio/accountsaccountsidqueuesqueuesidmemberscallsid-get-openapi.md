---
swagger: "2.0"
x-collection-name: Twilio
x-complete: 0
info:
  title: Twilio Get Queue Members
  description: Get a specific member.
  termsOfService: https://www.twilio.com/legal/tos
  version: v1
host: api.twilio.com
basePath: /2010-04-01/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Accounts/{AccountSid}/Calls/{CallSid}.{format}:
    get:
      summary: Get Call
      description: Get Call
      operationId: getCall
      x-api-path-slug: accountsaccountsidcallscallsid-format-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: CallSid
        description: A 34 character string that uniquely identifies the call
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Calls
  /Accounts/{AccountSid}/Calls.{format}:
    get:
      summary: Get Calls
      description: Get Calls
      operationId: getCalls
      x-api-path-slug: accountsaccountsidcalls-format-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Calls
    post:
      summary: Make Call
      description: To make a call, make an HTTP POST request. Initiate a new phone
        call.
      operationId: to-make-a-call-make-an-http-post-request-initiate-a-new-phone-call
      x-api-path-slug: accountsaccountsidcalls-format-post
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Calls
  /Accounts/{AccountSid}/Calls/{CallSid}/Recordings.{format}:
    get:
      summary: Get Recordings
      description: Returns a list of Recording resource representations, each representing
        anrecording generated during the course of a phone call.n
      operationId: returns-a-list-of-recording-resource-representations-each-representing-arecording-generated-during-t
      x-api-path-slug: accountsaccountsidcallscallsidrecordings-format-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: CallSid
        description: A 34 character string that uniquely identifies the call
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Recordings
  /Accounts/{AccountSid}/Conferences.{format}:
    get:
      summary: Get Conference Calls
      description: Returns a list of conferences within an account. The list includes
        pagingninformation.n
      operationId: returns-a-list-of-conferences-within-an-account-the-list-includes-paginginformation
      x-api-path-slug: accountsaccountsidconferences-format-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Conference Calls
  /Accounts/{AccountSid}/Conferences/{ConferenceSid}/Participants.{format}:
    get:
      summary: Get Conference Call Participants
      description: Returns the list of participants in the conference identified byn{ConferenceSid}.n
      operationId: returns-the-list-of-participants-in-the-conference-identified-byconferencesid
      x-api-path-slug: accountsaccountsidconferencesconferencesidparticipants-format-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: ConferenceSid
        description: A 34 character string that uniquely identifies the conference
          call object
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Conference Calls
  /Accounts/{AccountSid}/Conferences/{ConferenceSid}/Participants/{CallSid}.{format}:
    delete:
      summary: Delete Conference Call Participants
      description: Kick this participant from the conference.
      operationId: kick-this-participant-from-the-conference
      x-api-path-slug: accountsaccountsidconferencesconferencesidparticipantscallsid-format-delete
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: CallSid
        description: A 34 character string that uniquely identifies the call
      - in: path
        name: ConferenceSid
        description: A 34 character string that uniquely identifies the conference
          call object
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Conference Calls
    post:
      summary: Add Conference Call Participants
      description: Updates the status of a participant.
      operationId: updates-the-status-of-a-participant
      x-api-path-slug: accountsaccountsidconferencesconferencesidparticipantscallsid-format-post
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: CallSid
        description: A 34 character string that uniquely identifies the call
      - in: path
        name: ConferenceSid
        description: A 34 character string that uniquely identifies the conference
          call object
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Conference Calls
    get:
      summary: GetParticipantForConference
      description: GetParticipantForConference
      operationId: getparticipantforconference
      x-api-path-slug: accountsaccountsidconferencesconferencesidparticipantscallsid-format-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: CallSid
        description: A 34 character string that uniquely identifies the call
      - in: path
        name: ConferenceSid
        description: A 34 character string that uniquely identifies the conference
          call object
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
      responses:
        200:
          description: OK
      tags:
      - Conferences
  /Accounts/{AccountSid}/OutgoingCallerIds:
    get:
      summary: Get Outgoing Caller Ids
      description: Returns a list of OutgoingCallerId resource representations, each
        representingna Caller ID number valid for an account. The list includes paging
        information.n
      operationId: returns-a-list-of-outgoingcallerid-resource-representations-each-representinga-caller-id-number-vali
      x-api-path-slug: accountsaccountsidoutgoingcallerids-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      responses:
        200:
          description: OK
      tags:
      - Outgoing Caller IDs
    post:
      summary: Add Outgoing Caller Id
      description: Adds a new CallerID to your account.
      operationId: adds-a-new-callerid-to-your-account
      x-api-path-slug: accountsaccountsidoutgoingcallerids-post
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      responses:
        200:
          description: OK
      tags:
      - Outgoing Caller IDs
  /Accounts/{AccountSid}/OutgoingCallerIds/{OutgoingCallerIdSid}:
    get:
      summary: Get Outgoing Caller Ids
      description: Get the set of an accounts verified phone numbers.
      operationId: get-the-set-of-an-accounts-verified-phone-numbers
      x-api-path-slug: accountsaccountsidoutgoingcalleridsoutgoingcalleridsid-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: OutgoingCallerIdSid
        description: A 34 character string that uniquely identifies the outgoing caller
          id
      responses:
        200:
          description: OK
      tags:
      - Outgoing Caller IDs
    post:
      summary: Add Outgoing Caller Id
      description: Updates the caller id, and returns the updated resource if successful.
      operationId: updates-the-caller-id-and-returns-the-updated-resource-if-successful
      x-api-path-slug: accountsaccountsidoutgoingcalleridsoutgoingcalleridsid-post
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: OutgoingCallerIdSid
        description: A 34 character string that uniquely identifies the outgoing caller
          id
      responses:
        200:
          description: OK
      tags:
      - Outgoing Caller IDs
    put:
      summary: Update Outgoing Caller Id
      description: Updates the caller id, and returns the updated resource if successful.
      operationId: updates-the-caller-id-and-returns-the-updated-resource-if-successful
      x-api-path-slug: accountsaccountsidoutgoingcalleridsoutgoingcalleridsid-put
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: OutgoingCallerIdSid
        description: A 34 character string that uniquely identifies the outgoing caller
          id
      responses:
        200:
          description: OK
      tags:
      - Outgoing Caller IDs
    delete:
      summary: Delete Outgoing Caller ID
      description: DeleteOutgoingCallerId
      operationId: deleteoutgoingcallerid
      x-api-path-slug: accountsaccountsidoutgoingcalleridsoutgoingcalleridsid-delete
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
      - in: path
        name: OutgoingCallerIdSid
        description: A 34 character string that uniquely identifies the outgoing caller
          id
      responses:
        200:
          description: OK
      tags:
      - Outgoing Caller IDs
  /Accounts/{AccountSid}/Queues/{QueueSid}/Members/{CallSid}:
    get:
      summary: Get Queue Members
      description: Get a specific member.
      operationId: get-a-specific-member
      x-api-path-slug: accountsaccountsidqueuesqueuesidmemberscallsid-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: CallSid
        description: A 34 character string that uniquely identifies the call
      - in: path
        name: QueueSid
        description: A 34 character string that uniquely identifies the queue
      responses:
        200:
          description: OK
      tags:
      - Queues
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---