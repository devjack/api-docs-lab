---
title: Pets
type: endpoint
layout: single
endpoint: Pets
date: "2013-07-01"
lastmod: "2017-10-29"
operations:
  - url: "[{domain}](/guides/hypermedia)/pets"
    methods:
      - get
      - post
  - url: "[{domain}](/guides/hypermedia)/pets/{petId}"
    methods:
      - get
      - put
actions:
  list:
    example: '/examples/getPets.json'
  get:
    example: '/examples/getPet.json'
resource:
  name: Pet
  type: object
  properties:
    id:
      type: string
      format: uuid
      example: "d2014f64-ffdf-487b-8d12-67a20976aca6"
    name:
      type: string
      description: This is the name of the pet.
    tag:
      type: string
    owner:
      type: object
      description: Who owns this pet.
      properties:
        name:
          type: string
          description: The name of the owner
    uri:
      type: string
      x-guide: hypermedia
      example: "[{domain}](/guides/hypermedia)/pets/:id"
---

The Pet endpoint allows you to create, retrieve and update pet resources.
