<script setup>
const props = defineProps(['modalTitle', 'selectedAppForModal'])

const emit = defineEmits(['reset'])

const resetSelectedApp = () => emit('reset')

</script>

<template>
  <div class="modal fade" id="policy-modal" tabindex="-1" aria-hidden="true">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title ms-auto" id="policy-modal-label">{{ modalTitle }} Privacy Policy</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          <strong>Privacy Policy</strong>
          <p>This privacy policy applies to the {{ selectedAppForModal }} app (hereby referred to as "Application") for
            mobile devices
            that was created by Brandon Whisnant (hereby referred to as "Service Provider") as a Free service. This
            service
            is intended for use "AS IS".</p><br><strong>What information does the Application obtain and how is it
            used?</strong>
          <p>The Application does not obtain any information when you download and use it. Registration is not required
            to
            use the Application.</p><br><strong>Does the Application collect precise real time location information of
            the
            device?</strong>
          <p>This Application does not collect precise information about the location of your mobile device.</p>
          <br><strong>Do third parties see and/or have access to information obtained by the Application?</strong>
          <p>Since the Application does not collect any information, no data is shared with third parties.</p>
          <br><strong>What are my opt-out rights?</strong>
          <p>You can stop all collection of information by the Application easily by uninstalling it. You may use the
            standard uninstall processes as may be available as part of your mobile device or via the mobile application
            marketplace or network.</p><br><strong>Children</strong>
          <p>The Application is not used to knowingly solicit data from or market to children under the age of 13.</p>
          <br>
          <p>The Service Provider does not knowingly collect personally identifiable information from children. The
            Service
            Provider encourages all children to never submit any personally identifiable information through the
            Application
            and/or Services. The Service Provider encourage parents and legal guardians to monitor their children's
            Internet
            usage and to help enforce this Policy by instructing their children never to provide personally identifiable
            information through the Application and/or Services without their permission. If you have reason to believe
            that
            a child has provided personally identifiable information to the Service Provider through the Application
            and/or
            Services, please contact the Service Provider (bc.whisnant@gmail.com) so that they will be able to take the
            necessary actions. You must also be at least 16 years of age to consent to the processing of your personally
            identifiable information in your country (in some countries we may allow your parent or guardian to do so on
            your behalf).</p><br><strong>Security</strong>
          <p>The Service Provider is concerned about safeguarding the confidentiality of your information. However,
            since
            the Application does not collect any information, there is no risk of your data being accessed by
            unauthorized
            individuals.</p><br><strong>Changes</strong>
          <p>This Privacy Policy may be updated from time to time for any reason. The Service Provider will notify you
            of
            any changes to their Privacy Policy by updating this page with the new Privacy Policy. You are advised to
            consult this Privacy Policy regularly for any changes, as continued use is deemed approval of all changes.
          </p>
          <br>
          <p>This privacy policy is effective as of 2025-07-23</p><br><strong>Your Consent</strong>
          <p>By using the Application, you are consenting to the processing of your information as set forth in this
            Privacy
            Policy now and as amended by the Service Provider.</p><br><strong>Contact Us</strong>
          <p>If you have any questions regarding privacy while using the Application, or have questions about the
            practices,
            please contact the Service Provider via email at bc.whisnant@gmail.com.</p>
        </div>
        <div class="modal-footer">
          <button @click="resetSelectedApp" type="button" class="btn policy-modal-btn" data-bs-dismiss="modal">Close</button>
        </div>
      </div>
    </div>
  </div>

</template>

<style scoped>
.policy-modal-btn,
.policy-modal-btn:hover {
  border-radius: 2.5rem;
  background-color: rgb(222, 139, 93);
  color: rgb(255, 255, 255);
  background-image: linear-gradient(243deg, rgb(140, 81, 214) 0%, rgba(222, 139, 93, 0.008) 74%);
}
</style>
