---
title: Using a single encoder to tune COM1
description: Step-by-step guide to using a single encoder with integrated button to set the standby COM1 frequency.
ogimage: card-images/devices/encoder-single.png
---

Single rotary encoders with an integrated button are widely available and inexpensive, which makes them a popular option when building radio panels. Since radio frequencies consist of two parts, MHz and KHz, many people use the encoder push button to toggle whether the encoder controls the MHz or KHZ portion of the frequency.

The following steps show how to configure this in MobiFlight, using a MobiFlight variable to control which portion of the COM1 standby frequency gets adjusted by the encoder in a Cessna 172.

> [!NOTE]
> This guide assumes the encoder and button are already added as MobiFlight devices following the [encoder](/devices/encoder/) and [button](/devices/button-switch/) guides. It also assumes basic familiarity with creating MobiFlight input configurations.

{{% steps %}}

### Create an input configuration for the button

Name the configuration **COM1 KHz mode** and assign the **Device** to the encoder button. Set the **On Press** action to **MobiFlight - Variable** and the **Name** to **COM1 KHz mode**.

In the **Value** field, enter `($+1)%2`. This will cause the value of the variable to alternate between `0` and `1` on each button press.

{{< screenshot image="input-variable.png" title="Screenshot of an input configuration mapped to the encoder button, configured as a MobiFlight - Variable action type." >}}

The variable is used in the following steps as a precondition to disable input configurations based on the stored value.

### Create a MHz input configuration for the encoder

Name the configuration **COM1 standby - MHz** and assign the **Device** to the encoder knob.

Set the **On Left** action to **Microsoft Flight Simulator** and the preset to **COM_RADIO_WHOLE_DEC**. Assign the **On Right** action to **COM_RADIO_WHOLE_INC**.

{{< screenshot image="mhz-sim-variable.png" title="Screenshot of an input configuration, mapped to the encoder, configured as a Microsoft Flight Simulator action type and the On Left event assigned to the COM_RADIO_WHOLE_DEC preset." >}}

### Add a precondition to the MHz input configuration

On the **Precondition** tab for the **COM1 standby - MHz** config, click on **\<none\>** and change **Use type of** to **MobiFlight Variable**.

The variable created in step 1 should automatically be selected in the **Choose variable** dropdown. Use `0` for the **If current value is** comparison.

This will ensure the input configuration only runs when the **COM1 KHz mode** variable is set to `0`.

{{< screenshot image="mhz-precondition.png" title="Screenshot of the precondition tab with the COM1 KHz mode variable selected and the precondition set to = 0." >}}

### Create a KHz input configuration for the encoder

Name the configuration **COM1 standby - KHz** and assign the **Device** to the encoder knob.

Set the **On Left** action to **Microsoft Flight Simulator** and the preset to **COM_RADIO_FRACT_DEC**. Assign the **On Right** action to **COM_RADIO_FRACT_INC**.

{{< screenshot image="khz-sim-variable.png" title="Screenshot of an input configuration, mapped to the encoder, configured as a Microsoft Flight Simulator action type and the On Left event assigned to the COM_RADIO_FRACT_DEC preset." >}}

### Add a precondition to the KHz input configuration

On the **Precondition** tab for the **COM1 standby - KHz** config, click on **\<none\>** and change **Use type of** to **MobiFlight Variable**.

The variable created in step 1 should automatically be selected in the **Choose variable** dropdown. Use `1` for the **If current value is** comparison.

This will ensure the input configuration only runs when the **COM1 KHz mode** variable is set to `1`.

{{< screenshot image="khz-precondition.png" title="Screenshot of the precondition tab with the COM1 KHz mode variable selected and the precondition set to = 1." >}}

### Try it out

Spawn an airplane in Microsoft Flight Simulator. Make sure the MobiFlight **Run** button is clicked in the toolbar, then try adjusting the COM1 standby frequency with the encoder. By default, MHz should change, and pressing the encoder button should toggle to adjust KHz. Pressing the encoder button again will return to adjusting MHz.

MobiFlight will indicate which input configuration is disabled by the precondition by showing a red exclamation point at the start of the row. In the following screenshot, MHz adjustment is active and KHz adjustment is disabled.

{{< screenshot image="khz-disabled.png" title="Screenshot of the main MobiFlight window input tab with a red exclamation mark next to the COM1 standby - KHz row." >}}

{{% /steps %}}
