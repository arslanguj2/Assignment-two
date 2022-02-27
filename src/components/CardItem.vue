<template>
    <div class="col-md-6 col-sm-6 col-xs-12 col-lg-6">
        <div class="card mb-3">
            <div class="row g-0">
                <div class="col-md-5">
                    <img
                        :src="
                            'https://avatars.dicebear.com/v2/avataaars/' + user.username + '.svg?options[mood][]=happy'
                        "
                        class="img-fluid rounded-start"
                        :alt="`${user.username} profile image`"
                    />
                </div>
                <div class="col-md-7">
                    <div class="card-body position-relative">
                        <div class="user-id card-text position-absolute">ID # {{user.id}}</div>
                        <h5 class="card-title mb-1">{{user.name}}</h5>
                        <p class="card-text">
                            <small class="text-muted">@{{ user.username }}</small>
                        </p>
                        <p class="card-text">Website: {{ user.email }}</p>
                        <p class="card-text">Phone No: {{ user.phone }}</p>
                        <p class="card-text">Website: {{ user.website }}p></p>
                        <p class="card-text">Adress: {{ user.address.suite }}</p>
                        <p class="card-text">Street: {{ user.address.street }}</p>
                        <p class="card-text">Suite: {{ user.address.suite }}</p>
                        <p class="card-text">Zipcode: {{ user.address.zipcode }}</p>
                        <p class="card-text">Company: {{ user.company.name }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        user: { type: Object, required: true },
    },
};
</script>
