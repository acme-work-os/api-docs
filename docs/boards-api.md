# Boards API

> Synthetic demo content. Acme Work OS is a fictional product.

A board is a collection of items organised into columns. Boards belong to a workspace and can be public to the workspace or private to their members.

## List boards

`GET /v1/boards` returns the boards visible to the caller. Optional query parameters: `workspace_id`, `archived` (boolean) and `cursor`.

## Create a board

`POST /v1/boards` with a JSON body such as `{"name": "Q3 roadmap", "kind": "private"}`. The response contains the new board's `id` and `created_at` timestamp.

## Update a board

`PATCH /v1/boards/{id}` accepts any subset of `name`, `description` and `kind`. Fields that are omitted are left unchanged.

## Archive a board

`DELETE /v1/boards/{id}` archives the board. Archived boards can be restored for 30 days from the admin panel.
