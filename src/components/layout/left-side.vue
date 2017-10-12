<template>
    <!-- Left side column. contains the logo and sidebar -->
    <aside class="left-side sidebar-offcanvas">
        <!-- sidebar: style can be found in sidebar-->
        <section class="sidebar">
            <div id="menu" role="navigation">
                <div class="nav_profile">
                    <div class="media profile-left">
                        <a class="pull-left profile-thumb" href="javascript:void(0)">
                            <img :src="this.$store.state.user.picture" class="img-circle" alt="User Image">
                        </a>
                        <div class="content-profile">
                            <h4 class="media-heading user_name_max" v-text="this.$store.state.user.name"></h4>
                            <ul class="icon-list">
                                <li>
                                    <router-link to="/users_list" title="user" exact>
                                        <i class="ti-user"></i>
                                    </router-link>
                                </li>
                                <li>
                                    <router-link to="/lockscreen" title="lock" exact>
                                        <i class="ti-lock"></i>
                                    </router-link>
                                </li>
                                <li>
                                    <router-link to="/edit_user" title="settings" exact>
                                        <i class="ti-settings"></i>
                                    </router-link>
                                </li>
                                <li>
                                    <router-link to="/login" title="Login" exact>
                                        <i class="ti-shift-right"></i>
                                    </router-link>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
                <ul class="navigation">
                    <router-link to="/" tag="li" exact>
                        <a class="logo"><i class="menu-icon ti-desktop"></i><span class="mm-text">Dashboard </span></a>
                    </router-link>
                    <li class="menu-dropdown">
                        <a href="javascript:void(0)">
                            <i class="menu-icon ti-bar-chart"></i>
                            <span class="mm-text">Batch Trackig </span>
                            <span class="fa arrow"></span>
                        </a>
                        <ul class="sub-menu">
                            <router-link tag="li" to="/general_components" exact>
                                <a class="logo"><i class="fa fa-fw ti-view-list"></i><span class="mm-text"> Batch List</span></a>
                            </router-link>
                            <router-link tag="li" to="/buttons" exact>
                                <a class="logo"><i class="menu-icon ti-view-list-alt"></i><span class="mm-text"> Material Management</span></a>
                            </router-link>
                        </ul>
                    </li>
                    <li class="menu-dropdown">
                        <a href="javascript:void(0)">
                            <i class="menu-icon ti-briefcase"></i>
                            <span class="mm-text"> Tools</span>
                            <span class="fa arrow"></span>
                        </a>
                        <ul class="sub-menu">
                            <router-link tag="li" to="/pickers" exact>
                                <a class="logo"><i class="menu-icon fa fa-cog"></i><span class="mm-text"> Configuration </span></a>
                            </router-link>
                            <router-link tag="li" to="/grid_layout" exact>
                                <a class="logo"><i class="menu-icon ti-unlink"></i><span class="mm-text"> Error log</span></a>
                            </router-link>
                        </ul>
                    </li>
                </ul>
                <!-- / .navigation -->
            </div>
            <!-- menu -->
        </section>
        <!-- /.sidebar -->
    </aside>
</template>
<script>
export default {
    name: "left-side"
}
</script>
