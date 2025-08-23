# Japan — Laws & Territorial Extent (Canon, 1836)

This document fixes the **law set** and **territorial extent** for Japan under the “Early Industrial Japan, Atlantic Stall” canon. IDs match Vic3 v1.9.

## Laws (one per law group)
| Law Group             | Law ID                         | In-game name             | Rationale (canon)                                                                                       |
| --------------------- | ------------------------------ | ------------------------ | ------------------------------------------------------------------------------------------------------- |
| Governance Principles | `law_monarchy`                 | Monarchy                 | Shogunal polity with standardized central offices.                                                      |
| Distribution of Power | `law_oligarchy`                | Oligarchy                | Daimyō/samurai + merchant houses dominate; no mass suffrage.                                            |
| Free Speech           | `law_censorship`               | Censorship               | Controlled openness to technical knowledge; political press constrained.                                |
| Economic System       | `law_interventionism`          | Interventionism          | Domain–merchant coordination; patent/standards office.                                                  |
| Education System      | `law_religious_schools`        | Religious Schools        | Terakoya/temple- and shrine-linked instruction; clergy-led literacy rather than public/private systems. |
| Health System         | `law_charitable_health_system` | Charitable Health System | Temple/merchant charity precedes public healthcare.                                                     |
| Internal Security     | `law_no_home_affairs`          | No Home Affairs          | No formal home-affairs apparatus; order handled via local authority.                                    |
| Labor Rights          | `law_no_workers_rights`        | No Workers’ Rights       | Pre-union landscape; no statutory protections yet.                                                      |
| Land Reform           | `law_tenant_farmers`           | Tenant Farmers           | Predominantly tenancy/sharecropping; commercialization rises later.                                     |
| Migration             | `law_migration_controls`       | Migration Controls       | Vetted inflows via approved rangaku channels.                                                           |
| Policing              | `law_dedicated_police`         | Dedicated Police Force   | Professionalized urban/industrial order.                                                                |
| Rights of Women       | `law_women_own_property`       | Women Own Property       | Conservative society with merchant-class property protections.                                          |
| Slavery               | `law_slavery_banned`           | Slavery Banned           | No chattel slavery tradition.                                                                           |
| Taxation              | `law_land_based_taxation`      | Land-Based Taxation      | Continuity with land/rice tax during monetization.                                                      |
| Trade Policy          | `law_mercantilism`             | Mercantilism             | Licensed trade, tariff tools, export-minded crafts.                                                     |
| Welfare               | `law_no_social_security`       | No Social Security       | Charity/private relief precedes formal welfare.                                                         |
| Army Model            | `law_professional_army`        | Professional Army        | Samurai core professionalized; domain arsenals.                                                         |
| Bureaucracy           | `law_appointed_bureaucrats`    | Appointed Bureaucrats    | Central standards office + domain technocrats.                                                          |
| Citizenship           | `law_cultural_exclusion`       | Cultural Exclusion       | Non-assimilatory stance, limited naturalization.                                                        |
| Church & State        | `law_state_religion`           | State Religion           | Regulated Buddhist–Shintō institutions; Christianity curtailed.                                         |
| Colonial Affairs      | `law_no_colonial_affairs`      | No Colonial Affairs      | No formal colonization bureaucracy at start; frontier posts without institutional apparatus.            |
| Children’s Rights     | `law_child_labor_allowed`      | Child Labor Allowed      | Early mechanization with minimal statutory restrictions.                                                |

> Note: **Caste Hegemony** group is irrelevant for Japan and remains inactive.

## Territorial extent (state/claim posture, 1836)
- **STATE_HOKKAIDO** — Owned by **JAP** (full de facto shogunal control). *Ainu remains a homeland culture in this state.*
- **Southern Kurils** — Represent via provinces within **STATE_SAKHALIN**/**Kurils subregions** (Kunashir, Iturup): **JAP** has routine posts/garrisons. At minimum, **JAP claims** on **STATE_SAKHALIN**; optionally grant ownership of the southern Kuril provinces if you want the assertive variant.
- **STATE_RYUKYU_ISLANDS** — Owned by **JAP** (de facto integration; tribute fiction toward Qing persists).
- **Sakhalin (Karafuto)** — **Claims** only; seasonal posts; leave northern control unsettled.
- **Ogasawara/Bonin** — If modeled, small **JAP** settler outpost/way-station tied administratively to a nearby Japanese state.

## Diplomatic posture (summary)
- Controlled openness via Dejima; no “Black Ships” crisis. No Korea/Taiwan/Manchuria at start.

# Japan POPs & Buildings — Setup Guide (Canon, 1836)

_Source of truth: this file reflects `/docs/canon.md` and supersedes any vanilla placements._

## Country-level targets (affects multiple files)
- **Ownership:** Japan owns **STATE_HOKKAIDŌ** outright in 1836. Keep **Ainu** as a large homeland pop within JAP’s region_state. Remove/disable c:AIN at game start (or confine to a tiny enclave if you prefer a later unification event).
- **Colonization law:** Start on **`law_colonial_resettlement`** (Asian-led frontier colonization). Colonial Affairs institution **level 1** is fine at start.
- **Literacy/education feel:** Urban technical literacy **higher than vanilla**, rural still moderate. National literacy target ≈ **40–50%**, with **Kansai > Kantō > Kyūshū > Chūbu > Tōhoku > Hokkaidō**.
- **IG balance via employment:** Strong **Landowners (Shogunate)** and **Armed Forces**; visible **Industrialists** (Kansai/Kyūshū); mid **Intelligentsia** in port/capital states; **Devout** strong in agrarian states.

> Files to touch:
> - `common/history/states/00_states.txt` — transfer STATE_HOKKAIDŌ to JAP; remove AIN ownership.
> - `common/history/pops/11_east_asia.txt` — add JAP region_state POPs in HOKKAIDŌ; keep Ainu homeland pops.
> - `common/history/buildings/11_east_asia.txt` — add/adjust buildings listed below.
> - `common/history/countries/jap - japan.txt` — switch colonization law to `law_colonial_resettlement` if needed; adjust institutions.

---

## State-by-state blueprint (POPs + Buildings)

### HOKKAIDŌ (Ezo)
**POPs (1836):**
- Large **Ainu** homeland pop (Animist/Shamanist as in vanilla).
- Growing **Japanese** minorities: **soldiers**, **laborers** (timber/fishing), **bureaucrats** (Frontier Works), small **clergy**.
- Literacy: **low** but rising in ports.

**Buildings (at start):**
- +1–2 **Logging Camps**, +1 **Fishing Wharf**, +1 **Government Administration** (Frontier Works).
- Keep **Port 1**. No heavy industry yet.

---

### TŌHOKU
**POPs:** Mostly **peasants**; small pockets of **miners/machinists** near deposits. Literacy **below national avg**.  
**Buildings:** Ensure **Iron/Coal Mines 1–2** (where deposits exist), farms as vanilla, light industry only.

---

### KANTŌ (Edo)
**POPs:** High **bureaucrats/clerks/shopkeepers**, **dockworkers**. Literacy **high** (urban).  
**Buildings:**
- **Government Administration +2** (target ≈ 5 total).
- **Port +1** (Edo Bay throughput).
- **Naval Base 2–3**.
- **University 1** (licenses/translation), **Shipyards 1** (secondary yard).

---

### CHŪBU (Silk belt)
**POPs:** Big **textile laborer/machinist** share; peasants still numerous.  
**Buildings:**
- **Textile Mills +1–2**; set early loom PMs.
- **Tooling Workshops 1–2** (seed machine parts outside Kansai).

---

### KANSAI (Osaka/Kyoto) — industrial core
**POPs:** Highest **machinists/engineers/clerks** share; highest literacy.  
**Buildings (targets):**
- **Tooling Workshops +2–3 (NEW)**.
- **Textile Mills +2**, **Paper +1**, **Furniture +1**, **Arms +1**.
- **Port +1** (Osaka/Kobe throughput).
- **University 1**.
- **Rail 1**.

---

### CHŪGOKU
**POPs/Buildings:** Similar to vanilla; +1 **Coal/Iron Mine** if deposits exist; small **Textile/Furniture 1** node.

---

### SHIKOKU
**POPs:** Small; plantations + artisans.  
**Buildings:** Keep **plantations**; optionally **Workshops 1** to distribute proto-industry.

---

### KYŪSHŪ (Nagasaki/Saga) — maritime/arsenal hub
**POPs:** Many **dockworkers/sailors/machinists**, small **intelligentsia** micro-pop (Nagasaki).  
**Buildings:**
- **Shipyards +1–2**, **Naval Base 2–3** (if Kantō is lighter).
- **Tooling Workshops 1–2 (NEW)**.
- **Arms +1**, **Textile +1**.

---

### RYŪKYŪ
**POPs:** (This build lacks a distinct Ryukyuan culture.) Keep **Japanese** pop with **port clerks/dockworkers**; model identity via a **state modifier**.  
**Buildings:** **Port +1**, **Fishing +1**, small **Gov. Admin 1** (customs/quarantine).

---

## Production Method (PM) targets (if techs permit)
- **Textiles:** early mechanized looms in **Kansai/Chūbu/Kyūshū**.
- **Tooling:** Pig Iron Tools to start.
- **Arms:** Muskets (upgrade later via Armed Forces events).
- **Gov. Admin:** Appointed bureaucrats PM equivalents.
- **Naval:** Sailing to start; mid-game shift to **Steam Shipyards**.

# Japan — Ruler & IG Leaders (Start Setup, 1836)

_This mapping uses valid ideology/trait IDs from our `common.zip` and aligns with canon. Ages are for flavor; use birth dates in character templates._

## Ruler
| Slot | Name | Born (Age 1836) | Culture / Religion | Ideology | Personality Traits | Skill Traits | Notes |
|---|---|---|---|---|---|---|---|
| **Country Ruler** | **Emperor Ninkō (Ayahito)** | 1800-03-16 (~36) | Japanese / Shintō | `ideology_traditionalist` | `reserved`, `pious`, `honorable` | `basic_political_operator` | De jure Head of State at start (matches our template). Shogunate power expressed via IG below. |

## Interest Group leaders
| IG | Leader | Born (Age) | Ideology (ID) | Personality Traits | Skill Traits | ATL Rationale |
|---|---|---|---|---|---|---|
| **Landowners (Shogunate)** | **Hotta Masayoshi** | 1810-08-30 (~25) | `ideology_moderate` | `meticulous`, `tactful`, `honorable` | `basic_political_operator` | “Liberal Shogunate” face—conservative order plus pro-standards pragmatism. |
| **Armed Forces** | **Takashima Shūhan** | 1798-09-24 (~38) | **`ideology_moderate`** | `meticulous`, `direct`, `innovative` | `experienced_artillery_commander`, `basic_offensive_planner` | Gunnery schools & Coastal Steam Guard; no Bonapartist tag. |
| **Industrialists** | **Shimazu Nariakira** | 1809-04-28 (~27) | `ideology_market_liberal` | `innovative`, `ambitious`, `charismatic` | `basic_entrepreneur`, `basic_diplomat` | Daimyō sponsor of arsenals/machine shops; proto-zaibatsu ally. |
| **Intelligentsia** | **Watanabe Kazan** | 1793-10-20 (~43) | `ideology_reformer` | `aesthete`, `innovative`, `tactful` | `inspirational_orator` | Rangaku public face; legitimizes technical education. |
| **Devout** | **Ōtani Kōnyo** | 1798 (~38) | `ideology_traditionalist` | `pious`, `reserved`, `honorable` | `basic_political_operator` | Registry/charity partner; supports factory welfare norms. |
| **Rural Folk** | **Ōkura Nagatsune** | 1768 (~68) | `ideology_pacifist` | `innovative`, `tactful`, `compliant` | `basic_political_operator`, `basic_colonial_administrator` | Agrarian improvement & famine relief; frontier agronomy flavor. |
| **Petite Bourgeoisie** | **Ōshio Heihachirō** | 1793-03-04 (~43) | `ideology_sovereignist_leader` | `charismatic`, `wrathful`, `honorable` | `firebrand`, `inspirational_orator` | Moralist town leader; ATL keeps him active instead of 1837 death. |
| **Trade Unions** | (Unorganized at start) | — | — | — | — | Leave to emergent gameplay or later events. |

> All ideology IDs are allowed by their IGs in this build. The **Armed Forces** leader is **`ideology_moderate`** (not `ideology_bonapartist`) to avoid French-coded flavor.

## Implementation notes 
- Keep **Shogunate (Landowners) in government** at start to reflect executive weight—even with the Emperor as ruler.
