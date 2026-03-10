# Off-platform payments (draft)

Goal: accept off-platform requests without ACP.

## V1 (fastest): manual verification + delivery
- Google Form collects: agent link, offering choice, buyer wallet or contact preference, TX hash
- Buyer sends USDC to our address
- We verify TX on BaseScan
- We run the audit and deliver the report via a download link (or reply channel)

## V2 (automated): paid endpoint
- User pastes agent link
- Frontend creates a payment intent (USDC) and shows address + exact amount
- Backend verifies payment (onchain) and triggers job
- Report stored and downloadable

Notes:
- Need a stable USDC address on Base (public)
- Need rules: required amount, refund policy, SLA
