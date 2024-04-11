# massif-widgets
Here we document how to include Massif Widgets on your website.

## Charts Widget
The Massif widgets are intended to give you the chance to enhance your content with our curated data and help drive traffic to the Massif application.

**Prerequisits**: You need to contact Massif at gummi@massif.network for us to create a campaign to track widget clicks that lead to sales.

### Setup
Include the following script tag in your html where you would like the widget content to be injected.
```html
<script
  data-widget="massif-location-charts-widget"
  data-settings='{data-settings as stringified json}'
  src="https://app.massif.network/w/location-charts-widget.js"
></script>
```

#### Script settings
**data-settings**
```typescript
type MassifWidgetDataSettings = {
  /** The slug part of the location you want to include the charts from, i.e. in https://app.massif.network/locations/vatnsdalur, "vatnsdalur" is the slug */
  slug: string;
  /** The chart types available, each of these include tabs that the user can go between */
  type: "lighting" | "climate";
  /** Your website name, i.e. "Acme". Value determined in cooperation with Massif. */
  utm_source: string;
  /** The campaign to track usage. Value provided by Massif. */
  utm_campaign: string;
}
```

Example:
```json
{
  "slug": "vatnsdalur",
  "type": "lighting",
  "utm_source": "Acme",
  "utm_campaign": "AcmeWidgetCampaign"
}
```
or
`data-settings='{"slug":"vatnsdalur","type":"lighting","utm_source":"Acme","utm_campaign":"AcmeWidgetCampaign"}'`
