# Facebook AI Comment Reply

Scheduled prototype for the Dr-Emad Taha AI Facebook Page.

**Status: disabled by default.** No comments are published until Meta permissions and the AI provider are configured and REPLY_ENABLED is explicitly set to true.

## Setup
1. Configure GitHub Actions secrets: FB_PAGE_ID, FB_PAGE_TOKEN, AI_API_KEY.
2. Configure Actions variables: AI_BASE_URL (OpenAI-compatible endpoint), AI_MODEL, REPLY_ENABLED=false.
3. Verify Meta Page access permissions for reading comments and publishing replies. App review may be required.
4. Manually run the workflow and inspect logs before enabling publication.
5. Change REPLY_ENABLED to true only after tests.

This prototype polls recent posts/comments and checks for an existing Page reply. It does not guarantee coverage of all comments, instant replies, free AI inference, or continuous operation. GitHub scheduled workflows may be delayed. For production, add durable state, monitoring and moderation.
