<template>
  <section>
    <v-container fluid>
      <div class="event-details-background">
        <v-img :src="eventDetails.imageUrl" class="rounded-lg" height="480"></v-img>
        <div>
          <h4 class="font__24 font-weight-bold mt-5">{{ eventDetails.title }}</h4>
          <div class="d-inline-flex">
            <p class="font__16">Category: </p>
            <h4 class="font-weight-bold ml-2">  {{  eventDetails.category }}</h4>
          </div>
          <v-row>
            <v-col cols="12" lg="8" md="6" sm="12">
              <div>
                <div class="d-flex mt-4">
                  <div class="d-flex">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                      <rect width="24" height="24" fill="white" style="mix-blend-mode:multiply" />
                      <path
                        d="M19.5 3H16.5V1.5H15V3H9V1.5H7.5V3H4.5C3.675 3 3 3.675 3 4.5V19.5C3 20.325 3.675 21 4.5 21H19.5C20.325 21 21 20.325 21 19.5V4.5C21 3.675 20.325 3 19.5 3ZM19.5 19.5H4.5V9H19.5V19.5ZM19.5 7.5H4.5V4.5H7.5V6H9V4.5H15V6H16.5V4.5H19.5V7.5Z"
                        fill="#9B51E0" />
                    </svg>
                    <p class="mx-2">{{ formatDate(eventDetails.date) }}</p>
                  </div>
                  <div class="d-flex ml-6">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                      <rect width="24" height="24" fill="white" style="mix-blend-mode:multiply" />
                      <path
                        d="M12 22.5C9.9233 22.5 7.89323 21.8842 6.16652 20.7304C4.4398 19.5767 3.09399 17.9368 2.29927 16.0182C1.50455 14.0996 1.29661 11.9884 1.70176 9.95156C2.1069 7.91476 3.10693 6.04383 4.57538 4.57538C6.04383 3.10693 7.91476 2.1069 9.95156 1.70176C11.9884 1.29661 14.0996 1.50455 16.0182 2.29927C17.9368 3.09399 19.5767 4.4398 20.7304 6.16652C21.8842 7.89323 22.5 9.9233 22.5 12C22.5 14.7848 21.3938 17.4555 19.4246 19.4246C17.4555 21.3938 14.7848 22.5 12 22.5ZM12 3C10.22 3 8.47992 3.52785 6.99987 4.51678C5.51983 5.50571 4.36628 6.91132 3.68509 8.55585C3.0039 10.2004 2.82567 12.01 3.17294 13.7558C3.5202 15.5016 4.37737 17.1053 5.63604 18.364C6.89472 19.6226 8.49836 20.4798 10.2442 20.8271C11.99 21.1743 13.7996 20.9961 15.4442 20.3149C17.0887 19.6337 18.4943 18.4802 19.4832 17.0001C20.4722 15.5201 21 13.78 21 12C21 9.61306 20.0518 7.32387 18.364 5.63604C16.6761 3.94822 14.387 3 12 3Z"
                        fill="#9B51E0" />
                      <path d="M15.4425 16.5L11.25 12.3075V5.25H12.75V11.685L16.5 15.4425L15.4425 16.5Z"
                        fill="#9B51E0" />
                    </svg>
                    <p class="mx-2">
                      {{ formatTime(eventDetails.time) }}</p>
                  </div>
                </div>
                <div class="d-flex">
                  <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <rect width="24" height="24" fill="white" style="mix-blend-mode:multiply" />
                    <path
                      d="M12 13.5C11.2583 13.5 10.5333 13.2801 9.91662 12.868C9.29994 12.456 8.81929 11.8703 8.53546 11.1851C8.25163 10.4998 8.17737 9.74584 8.32206 9.01841C8.46676 8.29098 8.82391 7.6228 9.34836 7.09835C9.8728 6.5739 10.541 6.21675 11.2684 6.07205C11.9958 5.92736 12.7498 6.00162 13.4351 6.28545C14.1203 6.56928 14.706 7.04993 15.118 7.66661C15.5301 8.2833 15.75 9.00832 15.75 9.75C15.7489 10.7442 15.3534 11.6974 14.6504 12.4004C13.9474 13.1034 12.9942 13.4989 12 13.5ZM12 7.5C11.555 7.5 11.12 7.63196 10.75 7.87919C10.38 8.12643 10.0916 8.47783 9.92128 8.88896C9.75098 9.3001 9.70642 9.7525 9.79324 10.189C9.88006 10.6254 10.0943 11.0263 10.409 11.341C10.7237 11.6557 11.1246 11.87 11.5611 11.9568C11.9975 12.0436 12.4499 11.999 12.861 11.8287C13.2722 11.6584 13.6236 11.37 13.8708 11C14.118 10.63 14.25 10.195 14.25 9.75C14.2494 9.15346 14.0121 8.58155 13.5903 8.15973C13.1685 7.73792 12.5965 7.50066 12 7.5Z"
                      fill="#9B51E0" />
                    <path
                      d="M12 22.5L5.67338 15.0385C5.63746 14.9956 5.41223 14.6999 5.41223 14.6999C4.33141 13.2763 3.74748 11.5374 3.75001 9.75C3.75001 7.56196 4.6192 5.46354 6.16638 3.91637C7.71355 2.36919 9.81197 1.5 12 1.5C14.188 1.5 16.2865 2.36919 17.8336 3.91637C19.3808 5.46354 20.25 7.56196 20.25 9.75C20.2527 11.5367 19.6692 13.2749 18.5889 14.698L18.5878 14.6999C18.5878 14.6999 18.3628 14.9956 18.3293 15.0354L12 22.5ZM6.60938 13.7963C6.60938 13.7963 6.78443 14.0274 6.82433 14.077L12 20.1809L17.1825 14.0684C17.2154 14.027 17.3916 13.7942 17.3916 13.7942C18.2746 12.631 18.7517 11.2103 18.75 9.75C18.75 7.95979 18.0388 6.2429 16.773 4.97703C15.5071 3.71116 13.7902 3 12 3C10.2098 3 8.49291 3.71116 7.22704 4.97703C5.96117 6.2429 5.25001 7.95979 5.25001 9.75C5.24835 11.2111 5.72587 12.6325 6.60938 13.7963Z"
                      fill="#9B51E0" />
                  </svg>
                  <p class="mx-2">
                    {{ eventDetails.address }}</p>
                </div>
                <div class="d-flex">
                  <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <rect width="24" height="24" fill="white" style="mix-blend-mode:multiply" />
                    <path
                      d="M12 3C12.7417 3 13.4667 3.21993 14.0834 3.63199C14.7001 4.04404 15.1807 4.62971 15.4645 5.31494C15.7484 6.00016 15.8226 6.75416 15.6779 7.48159C15.5333 8.20902 15.1761 8.8772 14.6517 9.40165C14.1272 9.9261 13.459 10.2833 12.7316 10.4279C12.0042 10.5726 11.2502 10.4984 10.5649 10.2145C9.87971 9.93072 9.29404 9.45007 8.88199 8.83339C8.46993 8.2167 8.25 7.49168 8.25 6.75C8.25 5.75544 8.64509 4.80161 9.34835 4.09835C10.0516 3.39509 11.0054 3 12 3ZM12 1.5C10.9616 1.5 9.94661 1.80791 9.08326 2.38478C8.2199 2.96166 7.54699 3.7816 7.14963 4.74091C6.75227 5.70022 6.64831 6.75582 6.85088 7.77422C7.05345 8.79262 7.55346 9.72808 8.28769 10.4623C9.02192 11.1965 9.95738 11.6966 10.9758 11.8991C11.9942 12.1017 13.0498 11.9977 14.0091 11.6004C14.9684 11.203 15.7883 10.5301 16.3652 9.66674C16.9421 8.80339 17.25 7.78835 17.25 6.75C17.25 5.35761 16.6969 4.02226 15.7123 3.03769C14.7277 2.05312 13.3924 1.5 12 1.5Z"
                      fill="#9B51E0" />
                    <path
                      d="M19.5 22.5H18V18.75C18 18.2575 17.903 17.7699 17.7145 17.3149C17.5261 16.86 17.2499 16.4466 16.9017 16.0983C16.5534 15.7501 16.14 15.4739 15.6851 15.2855C15.2301 15.097 14.7425 15 14.25 15H9.75C8.75544 15 7.80161 15.3951 7.09835 16.0983C6.39509 16.8016 6 17.7554 6 18.75V22.5H4.5V18.75C4.5 17.3576 5.05312 16.0223 6.03769 15.0377C7.02226 14.0531 8.35761 13.5 9.75 13.5H14.25C15.6424 13.5 16.9777 14.0531 17.9623 15.0377C18.9469 16.0223 19.5 17.3576 19.5 18.75V22.5Z"
                      fill="#9B51E0" />
                  </svg>
                  <p class="mx-2"> {{ eventDetails.organizer?.name }}</p>
                </div>
              </div>
            </v-col>
            <v-col cols="12" lg="4" md="6" sm="12">
              <div>
                <h4>Contact Organizer</h4>
                <div class="mt-4">
                  <v-icon color="white" class="mr-4">mdi-email</v-icon>
                  <v-icon color="white" class="mr-4">mdi-twitter</v-icon>
                  <v-icon color="white" class="mr-4">mdi-instagram</v-icon>
                </div>
              </div>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="12" lg="8" md="6" sm="12">
              <div>
                <h5 class="mb-6 font__16 font-weight-bold">Event description</h5>
                <p class="">{{ eventDetails.description }}
                </p>
                <h5 class="mt-4 font__16 font-weight-medium my-6">Tickets Pricing</h5>
                <div class="d-flex">
                  <div>
                    <p class="font__20 font-weight-bold">Price</p>
                    <p class="font__16 primary--text font-weight-bold"> {{ eventDetails.price == 0 ? "FREE" :
                       eventDetails.price }}</p>
                  </div>
                </div>
                <v-btn color="#783EAD" class="mt-6 font__16 font-weight-bold white--text" depressed>Buy now</v-btn>
              </div>
            </v-col>
            <v-col cols="12" lg="4" md="6" sm="12">
              <div>
                <h5 class="mb-6 font__16 ">Direction</h5>
                <v-img height="452" src="/images/direction.png"></v-img>
              </div>
            </v-col>
          </v-row>
        </div>
      </div>
    </v-container>
  </section>
</template>

<script>
export default {
  props:{
    eventDetails: {
      type: Object
    }
  },
  data() {
    return {}
  },
  methods: {
    formatDate(dateString) {
      const date = new Date(dateString)
      const options = {
        weekday: 'long',
        month: 'long',
        day: 'numeric',
        year: 'numeric',
      }
      return date.toLocaleDateString('en-US', options)
    },
    formatTime(timeString) {
      const time = new Date(`1970-01-01T${timeString}`);
      const hours = time.getHours();
      const amPm = hours >= 12 ? 'P.M' : 'A.M';
      const formattedHours = hours % 12 || 12;
      return `${formattedHours}${amPm}`;
    },
    formatPrice(price) {
      return `₦${price.toLocaleString('en-NG', { minimumFractionDigits: 2, maximumFractionDigits: 2 })}`;
    },
  },
  }
</script>

<style lang="scss" scoped>
.v-icon.v-icon {
  background: #783EAD;
  padding: 4px;
  border-radius: 5px;
}
</style>
