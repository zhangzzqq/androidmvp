androidmvp
==========

MVP Android Example used to explain how to use this pattern in our Android apps. This code was created to support an article explanation:

[Android MVP @ antonioleiva.com (English)](http://antonioleiva.com/mvp-android)

[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-androidmvp-brightgreen.svg?style=flat)](https://android-arsenal.com/details/3/1514)



mvp-master app

LoginView 是与V层打交道
LoginInteractor 是与M层 接口打交道，最后的结果会反馈给P层
P层联系着V和M层，写的非常的好
跟之前的Wiicare项目非常的像
public class LoginContract {
    public interface View extends BaseView<Presenter> {
        boolean isActive();

        void gotoMainActivity();
    }

    public interface Presenter extends BasePresenter {
        void start();

        void login(String username, String password);
    }
}

只是Wiicare这个项目把 对应View层的接口层和与M数据相关的接口层Interactor写在一个类中