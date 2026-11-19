# Punjab travel and immigration agent licences, by district

District-level counts of the travel, immigration and IELTS agents listed on the official licence registers of Punjab (and Chandigarh and Panchkula), with how many hold a licence the register shows as currently valid, expired or cancelled.

Data as of **19 November 2026**. The live, regularly refreshed version, with a chart, key findings and a page for every agent, is at **[recepta.in/directory/statistics](https://recepta.in/directory/statistics)**.

## Headline figures

- **8,693** agents across **25** official registers.
- **2,962** hold a licence the register shows as currently valid.
- **825** licences are recorded as **cancelled**, mostly in Jalandhar (325), Moga (244) and Nawanshahr (96).
- **1,950** agents are on registers that publish no validity information at all (Ludhiana, Chandigarh).
- **10** districts last published a register more than two years ago.

## The file

[`data/punjab-travel-agent-licences-by-district.csv`](data/punjab-travel-agent-licences-by-district.csv), one row per district:

| Column | Meaning |
|---|---|
| `district` | District, as the register names it |
| `agents` | Entries on the register |
| `scanned_register` | `yes` when the register is a scanned image read by OCR (see limitations) |
| `validity_stated` | Entries whose register prints an expiry date or a cancellation |
| `valid` | Licence shown as currently valid |
| `expired` | Validity date printed in the register has passed |
| `cancelled` | Licence recorded as cancelled |
| `pct_valid_of_stated` | `valid` as a share of `validity_stated` |
| `register_published` | Date of the register edition counted |
| `fetched` | Date the register was downloaded |
| `source_url` | The government document the row was counted from |

A blank cell means the register does not say, never zero.

## How it is produced

Each district's register is downloaded from the government site that publishes it (district administrations under the Punjab Travel Professionals (Regulation) Act, the Chandigarh Police list, the Panchkula list), parsed row by row and counted. Nothing is edited by hand. Every row links its source document.

## Limitations, please read before quoting

- **Expired is not illegal.** Registers are republished only every so often, so an agent may have renewed since the edition counted. An expired date is a reason to ask for the current certificate, not a finding against the agent.
- **Cancelled is different.** A cancellation is recorded deliberately by the issuing authority.
- **Some registers say nothing about validity** (Ludhiana, Chandigarh). Their validity columns are blank.
- **Scanned registers** (`scanned_register = yes`) are read by OCR. Their dates can be misread, so validity is not counted for them. Cancellations written in those registers still are.
- **Old registers.** Where a register is several years old, most of its dates have passed, so its share of valid licences mostly reflects the document's age.

## Licence and citation

[CC BY 4.0](LICENSE). Free to use, including in reporting, with credit:

> Recepta analysis of official district travel-agent registers, Punjab and Chandigarh, data as of 19 November 2026. https://recepta.in/directory/statistics

Recepta is not a government body and does not issue, renew or cancel licences. To check a particular agent, search the register at [recepta.in/directory](https://recepta.in/directory).
