---
id: crowdsale_validation_PausableCrowdsale
title: PausableCrowdsale
---

<div class="contract-doc"><div class="contract"><h2 class="contract-header"><span class="contract-kind">contract</span> PausableCrowdsale</h2><p class="base-contracts"><span>is</span> <a href="crowdsale_Crowdsale.html">Crowdsale</a><span>, </span><a href="lifecycle_Pausable.html">Pausable</a></p><p class="description">Extension of Crowdsale contract where purchases can be paused and unpaused by the pauser role.</p><div class="source">Source: <a href="https://github.com/OpenZeppelin/zeppelin-solidity/blob/v2.1.2/contracts/crowdsale/validation/PausableCrowdsale.sol" target="_blank">crowdsale/validation/PausableCrowdsale.sol</a></div></div><div class="index"><h2>Index</h2><ul><li><a href="crowdsale_validation_PausableCrowdsale.html#_preValidatePurchase">_preValidatePurchase</a></li></ul></div><div class="reference"><h2>Reference</h2><div class="functions"><h3>Functions</h3><ul><li><div class="item function"><span id="_preValidatePurchase" class="anchor-marker"></span><h4 class="name">_preValidatePurchase</h4><div class="body"><code class="signature">function <strong>_preValidatePurchase</strong><span>(address _beneficiary, uint256 _weiAmount) </span><span>internal </span><span>view </span></code><hr/><div class="description"><p>Validation of an incoming purchase. Use require statements to revert state when conditions are not met. Use super to concatenate validations. Adds the validation that the crowdsale must not be paused.</p></div><dl><dt><span class="label-modifiers">Modifiers:</span></dt><dd><a href="lifecycle_Pausable.html#whenNotPaused">whenNotPaused </a></dd><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>_beneficiary</code> - Address performing the token purchase</div><div><code>_weiAmount</code> - Value in wei involved in the purchase</div></dd></dl></div></div></li></ul></div></div></div>