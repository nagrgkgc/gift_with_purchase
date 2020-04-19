# gift_with_purchase
gwp

gift with purchase<br/>
new cart rule with new action (free gift)<br/>
qty managed from cart rule<br/>
sku can be added from cart rule<br/>
managed cart conditions at PDP, CART, MINICART<br/>

Magento_Checkout/templates/cart/form.phtml<br/>
can delete cart gift product, can be added back again (missing template)<br/>

$flag = (int)$this->helper(Magento\Checkout\Helper\Data::class)->getCheckout()->getRemovedFreeProduct();
$giftApplicable = (int)$this->helper(Magento\Checkout\Helper\Data::class)->getCheckout()->getFreeGiftApplied();

if($flag && $giftApplicable){
 echo __('You are eligible for free gift.');?>&nbsp; rtrim($block->escapeUrl($block->getUrl('checkout/cart?fg=1')), '/') echo __('Add free gift to shopping bag.');
}

