# Enterprise Approval Flow

A finance analyst submits a vendor for approval. The page shows database statuses: pending_vendor_review, approved_l2, blocked_flag. The analyst cannot tell who owns the next step. Managers approve by clicking a generic "Update" button. There is no visible audit history.

Problems the skill should identify:
- backend language exposed in UI
- unclear owner and next approver
- unsafe generic approval action
- duplicated or derived blocker state
- missing audit visibility
- weak production safety
