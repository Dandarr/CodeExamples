<template>
    <div class="govuk-warning-text">
      <span class="govuk-warning-text__icon" aria-hidden="true">!</span>
      <strong class="govuk-warning-text__text">
        <span class="govuk-warning-text__assistive">Warning</span>
        {{WarningMessage}}
      </strong>
    </div>
</template>

<script>
export default {
	props: {
		WarningMessage: String,
	}
};
</script>