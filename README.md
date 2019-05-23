# ![LOGO](logo.png) Google Slides **flow**ground Connector

## Description

A generated **flow**ground connector for the Google Slides API (version v1).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/slides/v1/swagger.json<br/>
Generated at: 2019-05-23T12:13:40+03:00

## API Description

Reads and writes Google Slides presentations.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Creates a blank presentation using the title given in the request. If a<br/>
> `presentationId` is provided, it is used as the ID of the new presentation.<br/>
> Otherwise, a new ID is generated. Other fields in the request, including<br/>
> any provided content, are ignored.<br/>
> Returns the created presentation.

*Tags:* `presentations`

#### Input Parameters
* `$.xgafv` - _optional_ - V1 error format.
    Possible values: 1, 2.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets the latest version of the specified presentation.

*Tags:* `presentations`

#### Input Parameters
* `presentationId` - _required_ - The ID of the presentation to retrieve.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets the latest version of the specified page in the presentation.

*Tags:* `presentations`

#### Input Parameters
* `pageObjectId` - _required_ - The object ID of the page to retrieve.
* `presentationId` - _required_ - The ID of the presentation to retrieve.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Generates a thumbnail of the latest version of the specified page in the<br/>
> presentation and returns a URL to the thumbnail image.<br/>
> <br/>
> This request counts as an [expensive read request](/slides/limits) for<br/>
> quota purposes.

*Tags:* `presentations`

#### Input Parameters
* `pageObjectId` - _required_ - The object ID of the page whose thumbnail to retrieve.
* `presentationId` - _required_ - The ID of the presentation to retrieve.
* `thumbnailProperties.mimeType` - _optional_ - The optional mime type of the thumbnail image.

If you don't specify the mime type, the default mime type will be PNG.
    Possible values: PNG.
* `thumbnailProperties.thumbnailSize` - _optional_ - The optional thumbnail image size.

If you don't specify the size, the server chooses a default size of the
image.
    Possible values: THUMBNAIL_SIZE_UNSPECIFIED, LARGE, MEDIUM, SMALL.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Applies one or more updates to the presentation.<br/>
> <br/>
> Each request is validated before<br/>
> being applied. If any request is not valid, then the entire request will<br/>
> fail and nothing will be applied.<br/>
> <br/>
> Some requests have replies to<br/>
> give you some information about how they are applied. Other requests do<br/>
> not need to return information; these each return an empty reply.<br/>
> The order of replies matches that of the requests.<br/>
> <br/>
> For example, suppose you call batchUpdate with four updates, and only the<br/>
> third one returns information. The response would have two empty replies:<br/>
> the reply to the third request, and another empty reply, in that order.<br/>
> <br/>
> Because other users may be editing the presentation, the presentation<br/>
> might not exactly reflect your changes: your changes may<br/>
> be altered with respect to collaborator changes. If there are no<br/>
> collaborators, the presentation should reflect your changes. In any case,<br/>
> the updates in your request are guaranteed to be applied together<br/>
> atomically.

*Tags:* `presentations`

#### Input Parameters
* `presentationId` - _required_ - The presentation to apply the updates to.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-slides-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
