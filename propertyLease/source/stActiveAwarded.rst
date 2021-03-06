.. _stActiveAwarded:

Status: active.awarded
======================

Період внесення оплати учасником paymentPeriod
----------------------------------------------

Первинно на `paymentPeriod` виділяється до 20 днів від початку кваліфікації даного учасника, але період триває доти, доки Організатор не переведе `award` у наступний статус. Під час `paymentPeriod’у` Організатор має підтвердити отримання оплати від кваліфікованого учасника. Після отримання оплати Організатор переводить `award` в статус `active`, після чого для цього `award’у` створюється `contract` в статусі `pending`.

Період підписання контракту signingPeriod
-----------------------------------------

Первинно на `SigningPeriod` виділено до 20 днів від початку кваліфікації учасника, але період триває доти, доки Організатор не переведе процедуру в наступний статус. В межах `signingPeriod’у` організатор повинен завантажити та активувати контракт в системі.

Для другого учасника, одразу після аукціону, формується `award`, що отримує статус `pending.waiting`. У випадку, якщо ставка цього учасника була меншою аніж `value.amount+minimalStep`, цей авард одразу формується у статусі `unsuccessful`. Єдина дія, яка може бути виконана в цей момент - це ручне скасування очікування, учасник може перевести свій `award` в статус `cancelled`, після чого сплатити свій гарантійний внесок, втрачаючи шанс стати переможцем аукціону. Якщо перший `award` дискваліфіковують, а другий не самодискваліфікувався, останній автоматично змінює статус з `pending.waiting` на `pending.verification`, після чого учасник проходить процедуру кваліфікації по такому самому принципу як і його попередник. 	
