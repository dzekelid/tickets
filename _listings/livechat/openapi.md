swagger: "2.0"
x-collection-name: LiveChat
x-complete: 1
info:
  title: LiveChat REST API
  description: -introductionwelcome-to-the-livechat-api-documentationour-api-provides-a-set-of-flexible-tools-which-you-can-use-to-create-new-outstanding-projects--we-smile-a-bit-more-each-time-we-see-skilled-developers-unleash-their-creativityplease-note-that-this-documentation-refers-to-the-latest-api-version-2-0--if-you-are-looking-for-the-previous-version-check-out-the-deprecated-api-1-0-documentation--basic-api-usageall-livechat-api-requests-start-with--httpsapi-livechatinc-com-please-note-that-all-livechat-api-requests-must-use-https-protocol-the-next-segment-of-the-url-path-depends-on-the-type-of-your-request--for-example-use--httpsapi-livechatinc-comagents--to-get-or-modify-the-agents-data-all-requests-must-have-xapiversion-header-set-to-the-number-of-the-version-that-youd-like-to-use--the-most-recent-version-is-2--authenticationtwo-common-authentication-methods-are-supported--oauth-2-0--and--api-key--oauth-2-0oauth-2-0-authentication-is-the-recommended-way-of-authenticating-to-livechat-api-it-is-the-most-secure-way-of-making-api-calls--with-this-flow-you-will-get-access-only-to-some-parts-of-livechat-account-such-as-reading-agents-list--this-is-more-secure-than--api-key-flowhttpsdocs-livechatinc-comrestapiapikey--which-has-always-access-to-all-livechat-account-data-to-start-using-oauth-2-0-please-read-a-dedicated--authorizationhttpsdocs-livechatinc-comauthorization--guide--api-keyif-you-want-to-build-a-private-app-that-will-run-on-your-own-server-you-can-skip-the-oauth-2-0-flow-and-use-the-api-key--please-note-this-flow-of-making-api-calls-is-less-secure-because-the-api-key-gives-access-to-all-livechat-account-data-with-this-authorization-method-you-will-need-to-include-your-livechat-login-and--api-key--for-each-method-call--youll-find-the-api-key-in--your-livechat-profilehttpsmy-livechatinc-comagentsapikey-authentication-to-the-api-occurs-via--http-basic-authhttpen-wikipedia-orgwikibasic-access-authentication--provide-your--login--as-the-basic-auth-username-and-the--api-key--as-the-password--you-must-authenticate-for-all-requests-all-api-requests-must-be-made-over-https--data-formatthe-livechat-api-returns-the-data-in-the--jsonhttpen-wikipedia-orgwikijson--format--check-out-the-following-example--jsonpall-requests-made-with-http-get-are--jsonphttpen-wikipedia-orgwikijsonpenabled--to-use-jsonp-append--callback--and-the-name-of-your-callback-function-to-the-request--error-handlingthe-errors-are-returned-using-the-standard-http-error-code-syntax--in-general-the-codes-in-the-2xx-range-indicate-success-the-codes-in-the-4xx-range-indicate-an-error-incorrect-or-missing-parameters-not-authenticated-etc--and-the-codes-in-the-5xx-range-indicate-an-error-with-the-livechat-servers--any-additional-info-is-included-in-the-body-of-the-return-call-jsonformatted--http-status-codes-summary---400---the-request-is-incorrect-please-make-sure-that-the-passed-arguments-are-matching-the-format-in-the-methods-documentation----401---unauthorized--you-attempt-to-authenticate-with-an-invalid-username-or-api-key----404---not-found--you-attempt-to-request-a-resource-which-doesnt-exist----500---internal-server-error--something-unexpected-happened-on-our-end--please-try-again-or-contact-our-support--crossdomainall-crossdomain-api-requests-made-by-a-web-browser-are-denied-for-security-reasons--it-means-that-the-browserbased-requests-are-not-allowed-from-3rd-party-domains-including--localhost--livechat-api-librariesall-api-calls-include-an-api-key-that-can-be-easily-stolen-when-making-a-request-using-a-web-browser--it-means-you-should-use-backend-languages-for-api-requests--here-is-a-list-of-the-readytouse-libraries---php-library-for-livechat-apihttpsgithub-comlivechatapiclientphp-hosted-on-github----node-js-library-for-livechat-apihttpsgithub-comlivechatapiclientnodejs-hosted-on-github----ruby-library-for-livechat-apihttpsgithub-comcxzlivechat-client-hosted-on-github----c-library-for-livechat-apihttpsgithub-comlivechatapiclientcsharp-hosted-on-github--external-livechat-api-libraries---r-library-for-livechat-apihttpsgithub-comlawwulivechatr-hosted-on-github-did-you-write-your-own-library-and-want-it-listed-here-let-us-know
  version: 1.0.0
host: api.livechatinc.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /reports/tickets/new_tickets:
    get:
      summary: New tickets
      description: Shows the number of the tickets created during the specified period.
      operationId: ReportsTicketsNewTicketsGet
      x-api-path-slug: reportsticketsnew-tickets-get
      parameters:
      - in: query
        name: date_from
      - in: query
        name: date_to
      - in: query
        name: group_by
      - in: header
        name: X-API-Version
      responses:
        200:
          description: OK
      tags:
      - New
      - Tickets
  /reports/tickets/first_response_time:
    get:
      summary: Tickets first response time
      description: Shows the time of the first response to the tickets that were responded
        to for the first time during the specified period.
      operationId: ReportsTicketsFirstResponseTimeGet
      x-api-path-slug: reportsticketsfirst-response-time-get
      parameters:
      - in: query
        name: agent
      - in: query
        name: date_from
      - in: query
        name: date_to
      - in: header
        name: X-API-Version
      responses:
        200:
          description: OK
      tags:
      - Tickets
      - First
      - Response
      - Time
  /reports/tickets/resolution_time:
    get:
      summary: Tickets resolution time
      description: Shows the resolution time of the tickets that were solved during
        the specified period.
      operationId: ReportsTicketsResolutionTimeGet
      x-api-path-slug: reportsticketsresolution-time-get
      parameters:
      - in: query
        name: date_from
      - in: query
        name: date_to
      - in: header
        name: X-API-Version
      responses:
        200:
          description: OK
      tags:
      - Tickets
      - Resolution
      - Time
  /reports/tickets/solved_tickets:
    get:
      summary: Solved tickets
      description: Shows the number of the tickets solved during the specified period.
      operationId: ReportsTicketsSolvedTicketsGet
      x-api-path-slug: reportsticketssolved-tickets-get
      parameters:
      - in: query
        name: date_from
      - in: query
        name: date_to
      - in: header
        name: X-API-Version
      responses:
        200:
          description: OK
      tags:
      - Solved
      - Tickets
  /tickets:
    get:
      summary: Get list of tickets
      description: Returns all tickets.
      operationId: TicketsGet
      x-api-path-slug: tickets-get
      parameters:
      - in: query
        name: date_from
      - in: query
        name: status
      - in: header
        name: X-API-Version
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Tickets
    post:
      summary: Create a ticket
      description: Creates a new ticket.
      operationId: TicketsPost
      x-api-path-slug: tickets-post
      parameters:
      - in: formData
        name: message
      - in: formData
        name: requester[mail]
      - in: formData
        name: requester[name]
      - in: formData
        name: subject
      - in: header
        name: X-API-Version
      responses:
        200:
          description: OK
      tags:
      - Ticket
  /tickets/5FUED:
    get:
      summary: Get single ticket
      description: Returns a single ticket item for the given TICKET_ID
      operationId: Tickets5FUEDGet
      x-api-path-slug: tickets5fued-get
      parameters:
      - in: header
        name: X-API-Version
      responses:
        200:
          description: OK
      tags:
      - Single
      - Ticket
  /reports/tickets/ratings/ranking:
    get:
      summary: Ticket Ranking
      description: Shows the ratio of good to bad ratings for each operator.
      operationId: ReportsTicketsRatingsRankingGet
      x-api-path-slug: reportsticketsratingsranking-get
      parameters:
      - in: header
        name: X-API-Version
      responses:
        200:
          description: OK
      tags:
      - Ticket
      - Ranking
  /tickets/5FUED/tags:
    put:
      summary: Update ticket tags
      description: Updates tags associated with the ticket.
      operationId: Tickets5FUEDTagsPut
      x-api-path-slug: tickets5fuedtags-put
      parameters:
      - in: formData
        name: tag[]
      - in: header
        name: X-API-Version
      responses:
        200:
          description: OK
      tags:
      - Ticket
      - Tags
  /reports/tickets/ratings:
    get:
      summary: Ticket ratings report
      description: Shows the tickets that were rated during the specified period.
      operationId: ReportsTicketsRatingsGet
      x-api-path-slug: reportsticketsratings-get
      parameters:
      - in: query
        name: date_from
      - in: query
        name: date_to
      - in: query
        name: group
      - in: query
        name: group_by
      - in: header
        name: X-API-Version
      responses:
        200:
          description: OK
      tags:
      - Ticket
      - Ratings
      - Report
  /reports/tickets/ticket_sources:
    get:
      summary: Ticket sources
      description: Shows the distribution of the tickets between various channels.
      operationId: ReportsTicketsTicketSourcesGet
      x-api-path-slug: reportsticketsticket-sources-get
      parameters:
      - in: query
        name: date_from
      - in: query
        name: date_to
      - in: header
        name: X-API-Version
      responses:
        200:
          description: OK
      tags:
      - Ticket
      - Sources