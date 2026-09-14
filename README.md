# Facebook Ads MCP Server (Meta Ads) by Insightful Pipe

[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-blue)](https://insightfulpipe.com/mcp-servers/facebook-ads)
[![Insightful Pipe](https://img.shields.io/badge/Insightful_Pipe-MCP_Servers-purple)](https://insightfulpipe.com/mcp-servers)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Connect Facebook Ads and Instagram Ads to AI assistants with the Model Context Protocol (MCP).**

Part of the [Insightful Pipe MCP Server Collection](https://insightfulpipe.com/mcp-servers) — The Facebook Ads MCP server enables Claude, ChatGPT, Cursor, and other AI assistants to analyze your Meta advertising campaigns. Get AI-powered insights, automate reporting, and optimize your Facebook and Instagram ad performance.

[![Explore All MCP Servers](https://img.shields.io/badge/Explore_All-MCP_Servers-blue?style=for-the-badge)](https://insightfulpipe.com/mcp-servers)

![Facebook Ads MCP Server](https://insightfulpipe.com/images/meta-icon.svg)

## MCP Server URL

```
https://facebook-ads.insightfulmcp.com/
```

## What is Facebook Ads MCP?

Facebook Ads MCP is a **remote Model Context Protocol server** that connects your Meta Business Suite advertising data to AI assistants. This integration allows you to:

- Analyze Facebook and Instagram ad performance with natural language
- Get AI-powered optimization recommendations
- Monitor ROAS, CPM, CPC, and conversion metrics
- Create and manage campaigns and ad sets
- Search for targeting options and estimate audience sizes

## Installation

### Claude

1. Copy the MCP Server URL: `https://facebook-ads.insightfulmcp.com/`
2. Open [Claude Connectors Settings](https://claude.ai/settings/connectors)
3. Scroll to the bottom and click **Add custom connector**
4. Paste the URL and click **Add**
5. Click **Connect** on the connector to start authorization
6. Click **Authorize access** in the browser to complete the connection

### ChatGPT

Custom MCP servers are added through ChatGPT's **Developer mode**. Availability depends on your ChatGPT plan, and workspace admins may need to allow it.

1. Turn on **Developer mode** in ChatGPT settings
2. Create a new app for a remote MCP server and paste the URL: `https://facebook-ads.insightfulmcp.com/`
3. Authorize with your InsightfulPipe account

See OpenAI's guide: [Developer mode and MCP apps in ChatGPT](https://help.openai.com/en/articles/12584461-developer-mode-and-mcp-apps-in-chatgpt)

### Claude Code

```bash
claude mcp add --transport http facebook-ads https://facebook-ads.insightfulmcp.com/
```

### Cursor

Add the server to `~/.cursor/mcp.json` (all projects) or `.cursor/mcp.json` (one project):

```json
{
  "mcpServers": {
    "facebook-ads": {
      "url": "https://facebook-ads.insightfulmcp.com/"
    }
  }
}
```

Then authorize the connection when Cursor prompts you.

## Available Actions

67 actions: 41 read, 26 write.

### Read Actions (41)

<details>
<summary>Show all 41 read actions</summary>

| Action | Description |
|--------|-------------|
| `estimate_audience_size` | Estimate audience size for targeting specifications |
| `get_activities_adaccount` | Retrieve change history for an ad account |
| `get_activities_adset` | Retrieve change history for an ad set |
| `get_ad` | Fetch details for a single ad |
| `get_ad_creative` | Fetch details for a single ad creative |
| `get_ad_creatives` | List ad creatives for an ad account |
| `get_ad_creatives_by_ad` | Get the creative for a specific ad |
| `get_ad_images` | List ad images for an ad account |
| `get_ad_preview` | Generate a preview rendering for an existing ad |
| `get_ad_videos` | List ad videos for an ad account |
| `get_adaccount` | Fetch details for a single ad account |
| `get_ads` | List ads for an ad account, campaign, or ad set |
| `get_ads_by_adset` | List ads for a specific ad set |
| `get_ads_by_campaign` | List ads for a specific campaign |
| `get_adset` | Fetch details for a single ad set |
| `get_adsets` | List ad sets for an ad account or campaign |
| `get_adsets_by_campaign` | List ad sets for a specific campaign |
| `get_business_pixels` | List datasets (Meta Pixels) owned by a Business |
| `get_businesses` | List the Business Managers the connected user owns or manages |
| `get_campaign` | Fetch details for a single campaign |
| `get_campaigns` | List campaigns for an ad account |
| `get_catalogs` | List product catalogs owned by a Business |
| `get_custom_audiences` | List custom audiences for an ad account |
| `get_custom_conversion` | Get details for a specific custom conversion |
| `get_custom_conversions` | List custom conversions for an ad account |
| `get_insights_ad` | Retrieve performance insights for an ad |
| `get_insights_adaccount` | Retrieve performance insights for an ad account |
| `get_insights_adset` | Retrieve performance insights for an ad set |
| `get_insights_campaign` | Retrieve performance insights for a campaign |
| `get_instagram_accounts` | List Instagram accounts available to the selected ad account |
| `get_interest_suggestions` | Get interest suggestions based on existing interests |
| `get_leadgen_forms` | List lead generation forms for a Facebook Page |
| `get_leadgen_forms_by_account` | Discover lead generation forms already referenced by creatives in a Facebook ad account |
| `get_minimum_budgets` | List Meta's minimum budget values for the ad account by currency |
| `get_pages` | List Facebook Pages usable with this Ads connection in the selected workspace and brand |
| `get_pixels` | List tracking pixels for an ad account |
| `get_saved_audiences` | List saved audiences for an ad account |
| `search_behaviors` | Search for behavior targeting options by keyword |
| `search_demographics` | Search demographic targeting options |
| `search_geo_locations` | Search for geographic targeting locations |
| `search_interests` | Search for interest targeting options by keyword |

</details>

### Write Actions (26)

<details>
<summary>Show all 26 write actions</summary>

| Action | Description |
|--------|-------------|
| `assign_dataset_user` | Assign a user to a dataset |
| `connect_dataset` | Connect a dataset to an ad account and/or catalog |
| `create_ad` | Create a new ad (created in PAUSED status) |
| `create_ad_creative` | Create a new ad creative |
| `create_adset` | Create a new ad set (created in PAUSED status) |
| `create_campaign` | Create a new campaign (created in PAUSED status) |
| `create_catalog` | Create a product catalog in a Business |
| `create_custom_conversion` | Create a new custom conversion for an ad account |
| `create_dataset` | Create a dataset (Meta Pixel) in a Business |
| `create_leadgen_form` | Create a lead generation form on a Facebook Page |
| `create_product_feed` | Create a product feed inside a catalog |
| `create_product_item` | Create a product item inside a catalog |
| `create_product_set` | Create a product set inside a catalog |
| `delete_ad` | Permanently DELETE an ad |
| `delete_adset` | Permanently DELETE an ad set (and all its ads) |
| `delete_campaign` | Permanently DELETE a campaign (and all its ad sets + ads) |
| `update_ad` | Update an existing ad |
| `update_ad_creative` | Update an existing ad creative (name or labels only) |
| `update_adset` | Update an existing ad set |
| `update_campaign` | Update an existing campaign |
| `update_catalog` | Update a product catalog |
| `update_product_feed` | Update a product feed |
| `update_product_item` | Update a product item |
| `update_product_set` | Update a product set |
| `upload_ad_image` | Upload an image to the ad account from a public URL or base64-encoded bytes |
| `upload_ad_video` | Upload a video to the ad account from a URL or create a slideshow |

</details>

## Control What Your AI Can Do

You decide what AI agents can do with each connected account:

- **Turn individual actions on or off** for every connected account, so agents only see the actions you allow.
- **Connect as Read-only or Read & Write.** A read-only connection can only enable read actions.
- **Destructive actions stay off by default.** Actions such as deletes are disabled until an admin enables them.
- **Team access per account.** Restricted team members only use the accounts they are granted, with the read actions enabled on them.

New Meta campaigns are created **paused**, so nothing spends until you turn it on.

## Usage Examples

### Campaign Performance Analysis

```
"Show me my Facebook Ads performance for Q4 2024"
```

### Audience Insights

```
"Which audiences have the best ROAS on my Instagram campaigns?"
```

### Search for Targeting Options

```
"Search for interests related to 'fitness' for targeting"
```

### Estimate Audience Size

```
"Estimate the audience size for women 25-34 interested in yoga in California"
```

### Create Campaign

```
"Create a new conversions campaign called 'Holiday Sale' with a $100 daily budget"
```

## Supported Campaign Types

- **Awareness Campaigns** - Brand awareness and reach
- **Traffic Campaigns** - Website and app traffic
- **Engagement Campaigns** - Post engagement, page likes, event responses
- **Lead Generation** - Lead form campaigns
- **Sales Campaigns** - Catalog sales and conversions
- **App Promotion** - App installs and engagement

## Why Choose Facebook Ads MCP?

### For Social Media Marketers
- **Unified Meta analytics** - Facebook + Instagram in one place
- **Conversational reporting** - Ask questions, get answers
- **Time savings** - No more manual report building

### For E-commerce Brands
- **Catalog sales tracking** - Monitor product-level performance
- **ROAS optimization** - AI-driven budget recommendations
- **Audience discovery** - Find high-converting segments

### For Agencies
- **Multi-account support** - Manage client accounts efficiently
- **Automated reporting** - Generate client reports
- **Scalable workflows** - Handle more clients with AI

## Security & Compliance

- **Official Meta Marketing API** - Direct integration with Meta's API
- **OAuth 2.0** - Secure Meta authentication
- **Granular permissions** - Control read vs write access

## Pricing

The Facebook Ads MCP server is included in every InsightfulPipe plan, together with all other MCP servers and the CLI. Plans start at $29.99/month with a 7-day free trial. See [insightfulpipe.com/pricing](https://insightfulpipe.com/pricing) for current plans.

## Ready-Made Skills and Prompts

- [Claude skills for Meta Ads](https://insightfulpipe.com/marketing-claude-skills/facebook-ads) — ready-made skills that run on your connected data

## Explore More MCP Servers by Insightful Pipe

Visit **[insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)** to discover our full collection of MCP servers for marketing and analytics.

### Advertising MCP Servers
- [Google Ads MCP](https://insightfulpipe.com/mcp-servers/google-ads) - Google advertising
- [TikTok Ads MCP](https://insightfulpipe.com/mcp-servers/tiktok-ads) - TikTok advertising
- [LinkedIn Ads MCP](https://insightfulpipe.com/mcp-servers/linkedin-ads) - B2B advertising
- [Microsoft Ads MCP](https://insightfulpipe.com/mcp-servers/microsoft-ads) - Bing advertising
- [Pinterest Ads MCP](https://insightfulpipe.com/mcp-servers/pinterest-ads) - Pinterest advertising
- [Snapchat Ads MCP](https://insightfulpipe.com/mcp-servers/snapchat-ads) - Snapchat advertising

### Social Media MCP Servers
- [Instagram MCP](https://insightfulpipe.com/mcp-servers/instagram) - Organic Instagram analytics
- [YouTube MCP](https://insightfulpipe.com/mcp-servers/youtube) - YouTube analytics
- [Facebook Pages MCP](https://insightfulpipe.com/mcp-servers/facebook-pages) - Page management

**[View All MCP Servers →](https://insightfulpipe.com/mcp-servers)**

## Resources

- [Documentation](https://insightfulpipe.com/docs/connectors-facebook-ads)
- [Video Tutorial](https://www.youtube.com/playlist?list=PLJNzvjxzI5Xwe__BJJLAelSF0ewO3mEFk)
- [InsightfulPipe Blog](https://insightfulpipe.com/blog)

## Support

- **Documentation**: [insightfulpipe.com/docs](https://insightfulpipe.com/docs)
- **All MCP Servers**: [insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)
- **Email**: support@insightfulpipe.com

---

**[Insightful Pipe](https://insightfulpipe.com)** — AI-powered marketing analytics through MCP servers. [Explore all integrations →](https://insightfulpipe.com/mcp-servers)

## License

MIT License - see [LICENSE](LICENSE) for details.
