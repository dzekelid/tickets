---
swagger: "2.0"
x-collection-name: Eventbrite
x-complete: 0
info:
  title: Eventbrite Get Events Event Ticket Classes Ticket Class Ticket Groups
  description: |-
    Get the Ticket Groups for Ticket Class with the specified :ticket_class_id that belongs to the event with :event_id.
    By default, only the ticket groups that are live are shown.
  version: 1.0.0
host: www.eventbrite.com
basePath: /%7Bdata-type%7D/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /user_list_tickets:
    get:
      summary: Get User List Tickets
      description: This method lists the tickets purchased by the authenticated user.
        Each transaction is an order in our system and an order may contain one or
        more tickets. Tickets to free events are included.
      operationId: Get_user_list_tickets_
      x-api-path-slug: user-list-tickets-get
      parameters:
      - in: query
        name: data-type
        description: xml or json data-types are supported
      responses:
        200:
          description: OK
      tags:
      - User
      - List
      - Tickets
  /events/{id}/ticket_classes/:
    get:
      summary: Get Events Ticket Classes
      description: |-
        Returns a paginated response with a key of
        ticket_classes, containing a list of ticket_class.
      operationId: getEventsTicketClasses
      x-api-path-slug: eventsidticket-classes-get
      parameters:
      - in: query
        name: pos
        description: 'Only return ticket classes valid for the given point of sale
          (Valid choices are: online, or at_the_door)'
        type: query
      responses:
        200:
          description: OK
      tags:
      - Events
      - Ticket
      - Classes
    post:
      summary: Post Events Ticket Classes
      description: |-
        Creates a new ticket class, returning the result as a ticket_class
        under the key ticket_class.
      operationId: postEventsTicketClasses
      x-api-path-slug: eventsidticket-classes-post
      parameters:
      - in: query
        name: ticket_class.auto_hide
        description: Hide this ticket when it is not on sale
        type: query
      - in: query
        name: ticket_class.auto_hide_after
        description: Override re-hide date for auto-hide
        type: query
      - in: query
        name: ticket_class.auto_hide_before
        description: Override reveal date for auto-hide
        type: query
      - in: query
        name: ticket_class.cost
        description: Cost of the ticket (currently currency must match event currency)
          e
        type: query
      - in: query
        name: ticket_class.description
        description: Description of the ticket
        type: query
      - in: query
        name: ticket_class.donation
        description: Is this a donation? (user-supplied cost)
        type: query
      - in: query
        name: ticket_class.free
        description: Is this a free ticket?
        type: query
      - in: query
        name: ticket_class.hidden
        description: Hide this ticket
        type: query
      - in: query
        name: ticket_class.hide_description
        description: Hide the ticket description on the event page
        type: query
      - in: query
        name: ticket_class.include_fee
        description: Absorb the fee into the displayed cost
        type: query
      - in: query
        name: ticket_class.maximum_quantity
        description: Maximum number per order (blank for unlimited)
        type: query
      - in: query
        name: ticket_class.minimum_quantity
        description: Minimum number per order
        type: query
      - in: query
        name: ticket_class.name
        description: Name of this ticket type
        type: query
      - in: query
        name: ticket_class.order_confirmation_message
        description: Order message per ticket type
        type: query
      - in: query
        name: ticket_class.quantity_total
        description: Total available number of this ticket, required for non-donation
          tickets
        type: query
      - in: query
        name: ticket_class.sales_channels
        description: A list of all supported sales channels ([&#8220;online&#8221;],
          [&#8220;online&#8221;, &#8220;atd&#8221;], [&#8220;atd&#8221;])
        type: query
      - in: query
        name: ticket_class.sales_end
        description: When the ticket stops being on sale (leave empty for &#8216;one
          hour before event start&#8217;)
        type: query
      - in: query
        name: ticket_class.sales_start
        description: When the ticket is available for sale (leave empty for &#8216;when
          event published&#8217;)
        type: query
      - in: query
        name: ticket_class.sales_start_after
        description: The ID of another ticket class - when it sells out, this class
          will go on sale
        type: query
      - in: query
        name: ticket_class.split_fee
        description: Absorb the payment fee, but show the eventbrite fee
        type: query
      responses:
        200:
          description: OK
      tags:
      - Events
      - Ticket
      - Classes
  /events/{id}/ticket_classes/:ticket_class_id/:
    get:
      summary: Get Events Ticket Classes Ticket Class
      description: |-
        Gets and returns a single ticket_class by ID, as the key
        ticket_class.
      operationId: getEventsTicketClassesTicketClass
      x-api-path-slug: eventsidticket-classesticket-class-id-get
      responses:
        200:
          description: OK
      tags:
      - Events
      - Ticket
      - Classes
      - :ticket
      - Class
    post:
      summary: Post Events Ticket Classes Ticket Class
      description: Updates an existing ticket class, returning the updated result
        as a ticket_class under the key ticket_class.
      operationId: postEventsTicketClassesTicketClass
      x-api-path-slug: eventsidticket-classesticket-class-id-post
      parameters:
      - in: query
        name: ticket_class.auto_hide
        description: Hide this ticket when it is not on sale
        type: query
      - in: query
        name: ticket_class.auto_hide_after
        description: Override re-hide date for auto-hide
        type: query
      - in: query
        name: ticket_class.auto_hide_before
        description: Override reveal date for auto-hide
        type: query
      - in: query
        name: ticket_class.cost
        description: Cost of the ticket (currently currency must match event currency)
          e
        type: query
      - in: query
        name: ticket_class.description
        description: Description of the ticket
        type: query
      - in: query
        name: ticket_class.donation
        description: Is this a donation? (user-supplied cost)
        type: query
      - in: query
        name: ticket_class.free
        description: Is this a free ticket?
        type: query
      - in: query
        name: ticket_class.hidden
        description: Hide this ticket
        type: query
      - in: query
        name: ticket_class.hide_description
        description: Hide the ticket description on the event page
        type: query
      - in: query
        name: ticket_class.include_fee
        description: Absorb the fee into the displayed cost
        type: query
      - in: query
        name: ticket_class.maximum_quantity
        description: Maximum number per order (blank for unlimited)
        type: query
      - in: query
        name: ticket_class.minimum_quantity
        description: Minimum number per order
        type: query
      - in: query
        name: ticket_class.name
        description: Name of this ticket type
        type: query
      - in: query
        name: ticket_class.order_confirmation_message
        description: Order message per ticket type
        type: query
      - in: query
        name: ticket_class.quantity_total
        description: Total available number of this ticket, required for non-donation
          tickets
        type: query
      - in: query
        name: ticket_class.sales_channels
        description: A list of all supported sales channels ([&#8220;online&#8221;],
          [&#8220;online&#8221;, &#8220;atd&#8221;], [&#8220;atd&#8221;])
        type: query
      - in: query
        name: ticket_class.sales_end
        description: When the ticket stops being on sale (leave empty for &#8216;one
          hour before event start&#8217;)
        type: query
      - in: query
        name: ticket_class.sales_start
        description: When the ticket is available for sale (leave empty for &#8216;when
          event published&#8217;)
        type: query
      - in: query
        name: ticket_class.sales_start_after
        description: The ID of another ticket class - when it sells out, this class
          will go on sale
        type: query
      - in: query
        name: ticket_class.split_fee
        description: Absorb the payment fee, but show the eventbrite fee
        type: query
      responses:
        200:
          description: OK
      tags:
      - Events
      - Ticket
      - Classes
      - :ticket
      - Class
    delete:
      summary: Delete Events Ticket Classes Ticket Class
      description: 'Deletes the ticket class. Returns {&quot;deleted&quot;: true}.'
      operationId: deleteEventsTicketClassesTicketClass
      x-api-path-slug: eventsidticket-classesticket-class-id-delete
      parameters:
      - in: query
        name: break_dependency
        description: Delete even if ticket sales depend on this ticket
        type: query
      responses:
        200:
          description: OK
      tags:
      - Events
      - Ticket
      - Classes
      - :ticket
      - Class
  /events/:event_id/ticket_groups/:
    get:
      summary: Get Events Event Ticket Groups
      description: |-
        Get the list of ticket_group for the event with the specified :event_id.
        By default, only the ticket groups that are live are shown.
      operationId: getEventsEventTicketGroups
      x-api-path-slug: eventsevent-idticket-groups-get
      parameters:
      - in: query
        name: status
        description: 'Limits results to groups with the specific status (Valid choices
          are: live, archived, deleted, or all)'
        type: query
      responses:
        200:
          description: OK
      tags:
      - Events
      - :event
      - Ticket
      - Groups
  /events/:event_id/ticket_classes/:ticket_class_id/ticket_groups/:ticket_group_id/:
    post:
      summary: Post Events Event Ticket Classes Ticket Class Ticket Groups Ticket
        Group
      description: Add the Ticket Class with the specified :ticket_class_id that belongs
        to the event with :event_id to the Ticket Group identified by :ticket_group_id.
      operationId: postEventsEventTicketClassesTicketClassTicketGroupsTicketGroup
      x-api-path-slug: eventsevent-idticket-classesticket-class-idticket-groupsticket-group-id-post
      responses:
        200:
          description: OK
      tags:
      - Events
      - :event
      - Ticket
      - Classes
      - :ticket
      - Class
      - Ticket
      - Groups
      - :ticket
      - Group
    delete:
      summary: Delete Events Event Ticket Classes Ticket Class Ticket Groups Ticket
        Group
      description: Remove the Ticket Class with the specified :ticket_class_id that
        belongs to the event with :event_id from the Ticket Group identified by :ticket_group_id.
      operationId: deleteEventsEventTicketClassesTicketClassTicketGroupsTicketGroup
      x-api-path-slug: eventsevent-idticket-classesticket-class-idticket-groupsticket-group-id-delete
      responses:
        200:
          description: OK
      tags:
      - Events
      - :event
      - Ticket
      - Classes
      - :ticket
      - Class
      - Ticket
      - Groups
      - :ticket
      - Group
  /events/:event_id/ticket_classes/:ticket_class_id/ticket_groups/:
    get:
      summary: Get Events Event Ticket Classes Ticket Class Ticket Groups
      description: |-
        Get the Ticket Groups for Ticket Class with the specified :ticket_class_id that belongs to the event with :event_id.
        By default, only the ticket groups that are live are shown.
      operationId: getEventsEventTicketClassesTicketClassTicketGroups
      x-api-path-slug: eventsevent-idticket-classesticket-class-idticket-groups-get
      parameters:
      - in: query
        name: status
        description: 'Limits results to groups with the specific status (Valid choices
          are: live, archived, deleted, or all)'
        type: query
      responses:
        200:
          description: OK
      tags:
      - Events
      - :event
      - Ticket
      - Classes
      - :ticket
      - Class
      - Ticket
      - Groups
  /events/{id}/ticket_buyer_settings/:
    get:
      summary: Get Events Ticket Buyer Settings
      description: Returns a ticket_buyer_settings for an event.
      operationId: getEventsTicketBuyerSettings
      x-api-path-slug: eventsidticket-buyer-settings-get
      responses:
        200:
          description: OK
      tags:
      - Events
      - Ticket
      - Buyer
      - Settings
    post:
      summary: Post Events Ticket Buyer Settings
      description: Updates the ticket buyer settings for an event. Returns a ticket_buyer_settings.
      operationId: postEventsTicketBuyerSettings
      x-api-path-slug: eventsidticket-buyer-settings-post
      parameters:
      - in: query
        name: ticket_buyer_settings.confirmation_message.html
        description: Confirmation message to display on order completion
        type: query
      - in: query
        name: ticket_buyer_settings.instructions.html
        description: Instructions to display on the ticket
        type: query
      - in: query
        name: ticket_buyer_settings.redirect_url
        description: Redirect to this url post-purchase
        type: query
      - in: query
        name: ticket_buyer_settings.refund_request_enabled
        description: Whether refund requests are accepted for the event
        type: query
      responses:
        200:
          description: OK
      tags:
      - Events
      - Ticket
      - Buyer
      - Settings
  /ticket_groups/:ticket_group_id/:
    get:
      summary: Get Ticket Groups Ticket Group
      description: Returns the ticket_group with the specified :ticket_group_id.
      operationId: getTicketGroupsTicketGroup
      x-api-path-slug: ticket-groupsticket-group-id-get
      responses:
        200:
          description: OK
      tags:
      - Ticket
      - Groups
      - :ticket
      - Group
    delete:
      summary: Delete Ticket Groups Ticket Group
      description: |-
        Deletes the ticket_group with the specified :ticket_group_id.
        The status of the ticket group is changed to deleted.
      operationId: deleteTicketGroupsTicketGroup
      x-api-path-slug: ticket-groupsticket-group-id-delete
      responses:
        200:
          description: OK
      tags:
      - Ticket
      - Groups
      - :ticket
      - Group
    post:
      summary: Post Ticket Groups Ticket Group
      description: Updates the ticket group with the specified :ticket_group_id. Returns
        the updated ticket_group.
      operationId: postTicketGroupsTicketGroup
      x-api-path-slug: ticket-groupsticket-group-id-post
      parameters:
      - in: query
        name: ticket_group.event_ticket_ids
        description: (&#8216;IDs of tickets by event id for this ticket group
        type: query
      - in: query
        name: ticket_group.name
        description: Name of ticket group
        type: query
      - in: query
        name: ticket_group.status
        description: The status of ticket group
        type: query
      responses:
        200:
          description: OK
      tags:
      - Ticket
      - Groups
      - :ticket
      - Group
  /ticket_groups/:
    post:
      summary: Post Ticket Groups
      description: |-
        Creates a ticket group and returns the created ticket_group.
        Only up to 200 live ticket groups may be created; those with archived or deleted status are not taken into account.
      operationId: postTicketGroups
      x-api-path-slug: ticket-groups-post
      parameters:
      - in: query
        name: ticket_group.event_ticket_ids
        description: (&#8216;IDs of tickets by event id for this ticket group
        type: query
      - in: query
        name: ticket_group.name
        description: Name of ticket group
        type: query
      - in: query
        name: ticket_group.status
        description: The status of ticket group
        type: query
      responses:
        200:
          description: OK
      tags:
      - Ticket
      - Groups
  /users/:user_id/ticket_groups/:
    get:
      summary: Get Users User Ticket Groups
      description: |-
        Returns a paginated response of ticket_group for the specified user.
        The alias me (/users/me/) may be used to refer to the currently authenticated user.
      operationId: getUsersUserTicketGroups
      x-api-path-slug: usersuser-idticket-groups-get
      parameters:
      - in: query
        name: status
        description: 'Limits results to groups with the specific status (Valid choices
          are: live, archived, deleted, or all)'
        type: query
      responses:
        200:
          description: OK
      tags:
      - Users
      - :user
      - Ticket
      - Groups
  /users/:user_id/events/:event_id/ticket_classes/:ticket_class_id/ticket_groups/:
    post:
      summary: Post Users User Events Event Ticket Classes Ticket Class Ticket Groups
      description: |-
        Add the Ticket Class with the specified :ticket_class_id of the event with :event_id that
        belongs to the user with :user_id to many Ticket Groups specified with ticket_group_ids.
        If the list provided is empty, remove this ticket class from every ticket group.
      operationId: postUsersUserEventsEventTicketClassesTicketClassTicketGroups
      x-api-path-slug: usersuser-ideventsevent-idticket-classesticket-class-idticket-groups-post
      parameters:
      - in: query
        name: ticket_group_ids
        description: IDs of all ticket group this ticket belongs to
        type: query
      responses:
        200:
          description: OK
      tags:
      - Users
      - :user
      - Events
      - :event
      - Ticket
      - Classes
      - :ticket
      - Class
      - Ticket
      - Groups
  /ticket_new:
    get:
      summary: Get Ticket New
      description: This method creates new fixed-price or donation ticket types. It
        returns the ID of the newly created ticket.
      operationId: Get_ticket_new_
      x-api-path-slug: ticket-new-get
      parameters:
      - in: query
        name: data-type
        description: xml or json data-types are supported
      - in: query
        name: description
        description: The ticket description
      - in: query
        name: end_sales
        description: The date and time when ticket sales stop, in ISO 8601 format
          (e
      - in: query
        name: event_id
        description: The event ID
      - in: query
        name: include_fee
        description: 0 to add the Eventbrite service fee on top of ticket price, or
          1 to include it in the ticket price
      - in: query
        name: is_donation
        description: 0 for fixed-price tickets, 1 for donations
      - in: query
        name: max
        description: The maximum number of tickets per order
      - in: query
        name: min
        description: The minimum number of tickets per order
      - in: query
        name: name
        description: The ticket name
      - in: query
        name: price
        description: The ticket price
      - in: query
        name: quantity
        description: The number of tickets available
      - in: query
        name: start_sales
        description: The date and time when ticket sales start, in ISO 8601 format
          (e
      responses:
        200:
          description: OK
      tags:
      - Ticket
      - New
  /ticket_update:
    get:
      summary: Get Ticket Update
      description: This method updates an existing ticket type. Only the fields passed
        as arguments will be modified. It returns the ID of the updated ticket.
      operationId: Get_ticket_update_
      x-api-path-slug: ticket-update-get
      parameters:
      - in: query
        name: data-type
        description: xml or json data-types are supported
      - in: query
        name: description
        description: The ticket description
      - in: query
        name: end_sales
        description: The date and time when ticket sales stop, in ISO 8601 format
          (e
      - in: query
        name: hide
        description: Show or hide the ticket type
      - in: query
        name: id
        description: The ticket ID
      - in: query
        name: include_fee
        description: 0 to add the Eventbrite service fee on top of ticket price, or
          1 to include it in the ticket price
      - in: query
        name: is_donation
        description: 0 for fixed-price tickets, 1 for donations
      - in: query
        name: max
        description: The maximum number of tickets per order
      - in: query
        name: min
        description: The minimum number of tickets per order
      - in: query
        name: name
        description: The ticket name
      - in: query
        name: price
        description: The ticket price
      - in: query
        name: quantity
        description: The number of tickets available
      - in: query
        name: start_sales
        description: The date and time when ticket sales start, in ISO 8601 format
          (e
      responses:
        200:
          description: OK
      tags:
      - Ticket
      - Update
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