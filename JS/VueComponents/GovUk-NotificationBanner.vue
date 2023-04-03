<template>
    <div class="govuk-notification-banner" role="region" aria-labelledby="govuk-notification-banner-title" data-module="govuk-notification-banner">
  <div class="govuk-notification-banner__header">
    <h2 class="govuk-notification-banner__title" id="govuk-notification-banner-title">
        {{NotificationObject.NotificationTitle}}
    </h2>
  </div>
  <div class="govuk-notification-banner__content">
    <p class="govuk-notification-banner__heading">
      {{NotificationObject.NotificationMessage}}
      <a class="govuk-notification-banner__link" href="#">{{NotificationObject.NotificationLink}}</a>
    </p>
  </div>
</div>
</template>

<script>
export default {
  props:{ 
    NotificationObject:{
          NotificationMessage: String,
          NotificationTitle: String,
          NotificationLink:String
          }
    }
}
</script>