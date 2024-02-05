# Financial Tracking and Reporting Automation

## Rationale

The purpose of this automation is to streamline financial tracking and reporting by automatically creating an analytic account when a sale order is validated. This analytic account will play a crucial role in inventory valuation and associated journal entries.

## Specifications

### Part 1: Create Analytic Account per Sale Order (SO)

- When a sale order is validated, the system will automatically create an associated analytic account.
- The name of the analytic account will be generated and correspond to the SO name (e.g., SO/12345).
- In the event of a cancellation of a SO, the associated analytic account should be archived (never deleted).

### Part 2: Add Analytic Account to Journal Entry

- Considering the company's inventory valuation method (automated and costing method: average), a Journal Entry is created for each stock move.
- The analytic account linked to the Sale Order should be included in this inventory valuation journal entry.

### Part 3: Archive Analytic Account on SO Completion

- On the list of analytic accounts, an action is triggered to archive SOs that are marked as done.
- The system checks if the sale orders related to the existing analytic accounts are fully delivered, fully invoiced, and fully paid.
- If these conditions are met, the associated analytic account is archived.

## Usage

Follow the steps below to utilize this automation:

1. **Sale Order Validation:**

   - Upon validating a sale order, an analytic account will be automatically created and named according to the SO.

2. **Cancellation Handling:**

   - In the case of a canceled SO, the associated analytic account will be archived but not deleted.

3. **Journal Entry Integration:**

   - The analytic account linked to the sale order will be seamlessly integrated into the inventory valuation journal entries.

4. **Archive on SO Completion:**
   - To archive SOs, take action on the list of analytic accounts, marking them as done.
   - The system will automatically check and archive the analytic account if the associated SO is fully delivered, fully invoiced, and fully paid.

This automation ensures a robust and streamlined financial tracking system, enhancing the efficiency of inventory valuation and reporting processes.
