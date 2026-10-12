---
name: contact-agent
description: Help the user contact the agent or ask questions about a specific home. Use when the user wants to reach the seller or agent, book a viewing, ask about a listing, or asks for an agent's phone number or email, for a home found through Cubi Estate.
---

# Help the user reach the agent

Cubi runs contact with agents through its own consented flow. The connector never returns an agent's phone number or email, and calling it sends nothing to anyone.

1. Call `get_contact_options` with the listing's URL or id exactly as a result printed it, and the user's language.
2. Present the contact methods it lists (for example, sending the agent questions through Cubi, or a request by email that Cubi forwards) and the link it gives to start them. Mention who handles each one as the tool states, such as Cubi's team relaying the message, and that the link needs the user to sign in.
3. Offer the suggested questions it returns: these are things the listing does not already answer. Add any question the user has raised in the conversation.

## Be exact about what happened

- Nothing has been sent until the user follows one of the links and confirms there. Never say that you contacted the agent, booked a viewing or sent a message.
- If the user asks for the agent's phone number or email, explain that Cubi does not share agent contact details and offer the contact methods instead. Do not look for the details elsewhere.
