## Oomny B.V.

**Federatieve toegang over organisatiegrenzen heen. Voor de overheid, en nu ook voor AI-agents.**

Michael Owen Meijer, senior identity-architect en AI-engineer voor overheid en cloud.
Identity is de grens waar veilige AI begint.

**Identity, in productie bij de overheid.** IAM sinds 2011, federaties sinds 2015: voor een grote
bank, pensioenuitvoerders en de overheid, de laatste bijna acht jaar voor de vier grote gemeenten.
Entra ID, Keycloak (ingericht, cutover in voorbereiding), SAML en OIDC, SCIM, Conditional Access,
PIM, ADFS, MIM, Terraform.

**AI-engineering, als vakinhoud.** Agents met tool calling en MCP, RAG met vector search,
evaluatie en guardrails. Python, LangGraph, LangChain, Azure AI Foundry, Azure OpenAI, Azure AI
Search.

### AI-agents met een mandaat: begrensd, bewijsbaar, intrekbaar

Drie publieke demo's trekken dat identitywerk door naar AI-agents. Elke demo draait lokaal met
`make demo`, zonder API-sleutels, en bewaakt zijn grenzen met tests tegen de echte keten.

**Begrensd: [agent-mandaat](https://github.com/oomny-nl/agent-mandaat).** Een agent met een eigen
identiteit krijgt per taak een mandaat van één medewerker, en per actie een token van 60 seconden
voor één tool (OAuth 2.0 Token Exchange en DPoP op Keycloak). Een gekaapte agent komt niet buiten
dat mandaat. Er is ook een Entra Agent ID-variant in Terraform, in een lab-tenant uitgerold en
gemeten.

<a href="https://github.com/oomny-nl/agent-mandaat"><img src="https://raw.githubusercontent.com/oomny-nl/agent-mandaat/main/docs/beeld/demo.gif" alt="Demo agent-mandaat: toegestaan, buiten mandaat geweigerd, ingetrokken en noodstop" width="640"></a>

**Bewijsbaar: [agent-mandaatbewijs](https://github.com/oomny-nl/agent-mandaatbewijs).** Het
mandaat als verifieerbare credential (SD-JWT VC met een statuslijst, de bouwstenen van de
EUDI-wallet). Een register van een andere organisatie controleert het zonder account bij de
gemeente en zonder navraag per aanroep.

<a href="https://github.com/oomny-nl/agent-mandaatbewijs"><img src="https://raw.githubusercontent.com/oomny-nl/agent-mandaatbewijs/main/docs/beeld/demo.gif" alt="Demo agent-mandaatbewijs: toegestaan, replay, intrekking, niet-vertrouwde uitgever en noodstop" width="640"></a>

**Intrekbaar: [agent-levenscyclus](https://github.com/oomny-nl/agent-levenscyclus).**
Joiner-mover-leaver en recertificering voor agents: provisioning via SCIM, altijd een menselijke
eigenaar, autorisatie via OpenFGA. Vertrekt de eigenaar, dan wordt de agent bij zijn volgende
actie geweigerd.

<a href="https://github.com/oomny-nl/agent-levenscyclus"><img src="https://raw.githubusercontent.com/oomny-nl/agent-levenscyclus/main/docs/beeld/demo.gif" alt="Demo agent-levenscyclus: joiner, mover, leaver en verlopen agent" width="640"></a>

Standpunten: agents verdienen dezelfde zorg als mensen · open source waar het kan · federatie boven
synchronisatie · AI versnelt, identity begrenst.

[www.oomny.nl](https://www.oomny.nl) · michael@oomny.nl ·
[LinkedIn](https://www.linkedin.com/in/momeijer) · Den Haag, KvK 88737365 · beschikbaar per
1 januari 2027
