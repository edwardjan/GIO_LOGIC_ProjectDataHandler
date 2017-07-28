package logic;

import java.util.ArrayList;

import data.Project;

public class ProjectDataHandler {
	DatabaseManager db;
	ProjectListQuery prj;

	public ProjectDataHandler() {
		db = new DatabaseManager();
		prj = new ProjectListQuery();
	}

	public ArrayList<Project> getProcessedProjectList() {
		ArrayList<Project> temp = null;
		try {
			temp = db.getData(prj.getProjectListQuery());
		} catch (Exception e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
		return temp;
	}

//	public Project getProjectDetails(String projectID) {
//		// TODO Auto-generated method stub
//
//		Project temp = null;
//		try {
//			temp = db.getData(prj.getProjectListQuery());
//		} catch (Exception e) {
//			// TODO Auto-generated catch block
//			e.printStackTrace();
//		}
//		return temp;
//	}
}
