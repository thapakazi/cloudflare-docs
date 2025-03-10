---
pcx-content-type: how-to
type: overview
title: Filters
weight: 40
layout: list
---

# Filters

The following table represents the comparison operators that are supported and example values. Filters are added as escaped JSON strings formatted as `{"key":"<field>","operator":"<comparison_operator>","value":"<value>"}`.

- Refer to the [Log fields](/logs/reference/log-fields/) page for a list of fields related to each dataset.

- Comparison operators define how values must relate to fields in the log line for an expression to return true.

- Values represent the data associated with fields.

{{<table-wrap style="width:100%">}}

<table style='width:100%'>
  <thead>
   <tr>
      <th>Name</th>
      <th colspan="1" style="text-align:center">Operator Notation</th>
      <th colspan="5" style="text-align:center">Supported Field Types</th>
      <th></th>
   </tr>
   <tr>
      <td></td>
      <th>English</th>
      <th>String</th>
      <th>Int</th>
      <th>Bool</th>
      <th>Array</th>
      <th>Object</th>
      <th>Example (operator in bold)</th>
   </tr>
  </thead>
  <tbody>
    <tr>
      <td>Equal</td>
      <td><code class="InlineCode">eq</code></td>
      <td>&#x2705;</td>
      <td>&#x2705;</td>
      <td>&#x2705;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>
         <code class="InlineCode">{\"key\":\"ClientRequestHost\",\"operator\":\"<strong>eq</strong>\",\"value\":\"example.com\"}</code>
      </td>
     </tr>
    <tr>
      <td>Not equal</td>
      <td><code class="InlineCode">!eq</code></td>
      <td>&#x2705;</td>
      <td>&#x2705;</td>
      <td>&#x2705;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>
         <code class="InlineCode">{\"key\":\"ClientCountry\",\"operator\":\"<strong>!eq</strong>\",\"value\":\"ca\"}</code>
      </td>
    </tr>
    <tr>
      <td>Less than</td>
      <td><code class="InlineCode">lt</code></td>
      <td>&#10060;</td>
      <td>&#x2705;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>
         <code class="InlineCode">{\"key\":\"BotScore\",\"operator\":\"<strong>lt</strong>\",\"value\":\"30\"}</code>
      </td>
   </tr>
   <tr>
      <td>Less than<br />or equal</td>
      <td><code class="InlineCode">lte</code></td>
      <td>&#10060;</td>
      <td>&#x2705;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>
         <code class="InlineCode">{\"key\":\"BotScore\",\"operator\":\"<strong>lte</strong>\",\"value\":\"30\"}</code>
      </td>
    </tr>
    <tr>
      <td>Greater than</td>
      <td><code class="InlineCode">gt</code></td>
      <td>&#10060;</td>
      <td>&#x2705;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>
         <code class="InlineCode">{\"key\":\"BotScore\",\"operator\":\"<strong>gt</strong>\",\"value\":\"30\"}</code>
      </td>
    </tr>
    <tr>
      <td>Greater than<br />or equal</td>
      <td><code class="InlineCode">gte</code></td>
      <td>&#10060;</td>
      <td>&#x2705;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>
         <code class="InlineCode">{\"key\":\"BotScore\",\"operator\":\"<strong>gte</strong>\",\"value\":\"30\"}</code>
      </td>
    </tr>
    <tr>
      <td>Starts<br />with</td>
      <td><code class="InlineCode">startsWith</code></td>
      <td>&#x2705;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>
         <code class="InlineCode">{\"key\":\"ClientRequestPath\",\"operator\":\"<strong>startsWith</strong>\",\"value\":\"/foo\"}</code>
      </td>
    </tr>
    <tr>
      <td>Ends<br />with</td>
      <td><code class="InlineCode">endsWith</code></td>
      <td>&#x2705;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>
         <code class="InlineCode">{\"key\":\"ClientRequestPath\",\"operator\":\"<strong>endsWith</strong>\",\"value\":\"/foo\"}</code>
      </td>
    </tr>
    <tr>
      <td>Does not<br />start with</td>
      <td><code class="InlineCode">!startsWith</code></td>
      <td>&#x2705;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>
         <code class="InlineCode">{\"key\":\"ClientRequestPath\",\"operator\":\"<strong>!startsWith</strong>\",\"value\":\"/foo\"}</code>
      </td>
    </tr>
    <tr>
      <td>Does not<br />end with</td>
      <td><code class="InlineCode">!endsWith</code></td>
      <td>&#x2705;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>
         <code class="InlineCode">{\"key\":\"ClientRequestPath\",\"operator\":\"<strong>!endsWith</strong>\",\"value\":\"/foo\"}</code>
      </td>
    </tr>
    <tr>
      <td>Contains</td>
      <td><code class="InlineCode">contains</code></td>
      <td>&#x2705;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>&#x2705;</td>
      <td>&#10060;</td>
      <td>
         <code class="InlineCode">{\"key\":\"ClientRequestPath\",\"operator\":\"<strong>contains</strong>\",\"value\":\"/static\"}</code>
      </td>
    </tr>
    <tr>
      <td>Does not<br />contain</td>
      <td><code class="InlineCode">!contains</code></td>
      <td>&#x2705;</td>
      <td>&#10060;</td>
      <td>&#10060;</td>
      <td>&#x2705;</td>
      <td>&#10060;</td>
      <td>
         <code class="InlineCode">{\"key\":\"ClientRequestPath\",\"operator\":\"<strong>!contains</strong>\",\"value\":\"/static\"}</code>
      </td>
    </tr>
    <tr>
      <td>Value is in<br />a set of values</td>
      <td><code class="InlineCode">in</code></td>
      <td>&#x2705;</td>
      <td>&#x2705;</td>
      <td>&#10060;</td>
      <td>&#x2705;</td>
      <td>&#10060;</td>
      <td>
         <code class="InlineCode">{\"key\":\"EdgeResponseStatus\",\"operator\":\"<strong>in</strong>\",\"value\":[200,201]}</code>
      </td>
    </tr>
    <tr>
      <td>Value is not<br />in a set of values</td>
      <td><code class="InlineCode">!in</code></td>
      <td>&#x2705;</td>
      <td>&#x2705;</td>
      <td>&#10060;</td>
      <td>&#x2705;</td>
      <td>&#10060;</td>
      <td>
         <code class="InlineCode">{\"key\":\"EdgeResponseStatus\",\"operator\":\"<strong>!in</strong>\",\"value\":[200,201]}</code>
      </td>
    </tr>
  </tbody>
</table>
{{</table-wrap>}}

The filter field has limits of approximately 30 operators and 1000 bytes. Anything exceeding this value will return an error.

{{<Aside type="note" header="Note">}}
Filtering is not supported on the following data types: `objects`, `array[int]`, `array[object]`.

For the Firewall events dataset, the following fields are not supported: Action, Kind, MatchIndex, Metadata, OriginatorRayID, RuleID and Source.

For the Gateway HTTP dataset, the following fields are not supported: Downloaded File Names, Uploaded File Names.
{{</Aside>}}

## Logical Operators

- Filters can be connected using `AND`, `OR` logical operators.

- Logical operators can be nested.

Here are some examples of how the logical operators can be implemented. `X`, `Y` and `Z` are used to represent filter criteria:

- X AND Y AND Z - `{"where":{"and":[{X},{Y},{Z}]}}`

- X OR Y OR Z - `{"where":{"or":[{X},{Y},{Z}]}}`

- X AND (Y OR Z) - `{"where":{"and":[{X}, {"or":[{Y},{Z}]}]}}`

- (X AND Y) OR Z - `{"where":{"or":[{"and": [{X},{Y}]},{Z}]}}`

Example request using cURL:

```bash
curl -s -X POST https://api.cloudflare.com/client/v4/zones/<ZONE_ID>/logpush/jobs/ \
-H 'X-Auth-Key: <KEY>' \
-H 'X-Auth-Email:<EMAIL>' \
-H 'Content-Type: application/json' \
-d '{
"name":"example.com static assets",
"logpull_options":"fields=RayID,ClientIP,EdgeStartTimestamp&timestamps=rfc3339&CVE-2021-44228=true",
"dataset": "http_requests",
"filter":"{\"where\":{\"and\":[{\"key\":\"ClientRequestPath\",\"operator\":\"contains\",\"value\":\"/static\"},{\"key\":\"ClientRequestHost\",\"operator\":\"eq\",\"value\":\"example.com\"}]}}",
"destination_conf": "s3://<BUCKET_PATH>?region=us-west-2/"
}' | jq .
```